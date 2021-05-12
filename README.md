#include <iostream>
#include <ctime>
using namespace std;
void massiv_1(int arr[20], int numb)
{
	setlocale(LC_ALL, "ru");
	cout << "Введите элементы массива" << endl;
	for (int i = 0; i < numb; i++)
	{
		cout << "arr" << i << ": ";
		cin >> arr[i];
	}
	for (int i = 0; i < numb; i++)
	{
		cout << arr[i] << endl;
	}
}
void massiv_2(int arr[100][100], int numb)
{
	setlocale(LC_ALL, "ru");
	srand(time(NULL));
	for (int i = 0; i < numb; i++)
	{
		for (int j = 0; j < numb; j++)
		{
			arr[i][j] = 30 + rand() % 31;
		}
	}
	for (int i = 0; i < numb; i++)
	{
		for (int j = 0; j < numb; j++)
		{
			cout << arr[i][j] << "\t";
		}
		cout << endl;
	}
}
void minimum_2(int arr[100][100], int numb)
{
	int min = arr[0][0];
	for (int i = 0; i < numb; i++)
	{
		for (int j = 0; j < numb; j++)
		{
			if (arr[i][j] < min)
				min = arr[i][j];
		}
	}
	cout << min << endl;
}
void maximum_2(int arr[100][100], int numb)
{
	int max = arr[0][0];
	for (int i = 0; i < numb; i++)
	{
		for (int j = 0; j < numb; j++)
		{
			if (arr[i][j] > max)
				max = arr[i][j];
		}
	}
	cout << max << endl;
}
void massiv_3(int arr[100][100], int rows, int cols)
{
	setlocale(LC_ALL, "ru");
	cout << "Введите элементы массива" << endl;
	for (int i = 0; i < rows; i++)
	{
		for (int j = 0; j < cols; j++)
		{
			cout << "arr" << i << j << ": ";
			cin >> arr[i][j];
		}
	}
	for (int i = 0; i < rows; i++)
	{
		for (int j = 0; j < cols; j++)
		{
			cout << arr[i][j] << "\t";
		}
		cout << endl;
	}
}
int main()
{
	setlocale(LC_CTYPE, "Russian");
	int k = 0;
	while (k != 4)
	{
		cout << "Выберите программу" << endl;
		cout << "1) Объявить два целочисленных массива с разными размерами и написать функцию, которая заполняет их элементы значениями и показывает на экран. Функция должна принимать два параметра - масcив и его размер." << endl;
		cout << "2) Создать двумерный массив 5х5. Написать функцию, которая заполнит его случайными числами от 30 до 60. Создать еще две функции, которые находят максимальный и минимальный элементы этого двумерного массива." << endl;
		cout << "3) Дана целочисленная матрица A(N, M). Вычислите сумму и произведение нечётных отрицательных элементов матрицы, удовлетворяющих условию | ai j | < i." << endl;
		cout << "4) Завершить программу" << endl;
		cin >> k;
		if (k == 1)
		{
			setlocale(LC_CTYPE, "Russian");
			int k = 0, k2 = 0, a[20], a2[20];
			cout << "Введите размер массива1: ";
			cin >> k;
			massiv_1(a, k);
			cout << "Введите размер массива2: ";
			cin >> k2;
			massiv_1(a2, k2);
			cout << endl;
		}
		if (k == 2)
		{
			setlocale(LC_CTYPE, "Russian");
			int a[100][100];
			int const n = 5;
			massiv_2(a, n);
			cout << "Минимальный элемент массива: ";
			minimum_2(a, n);
			cout << "Максимальный элемент массива: ";
			maximum_2(a, n);
			cout << endl;
		}
		if (k == 3)
		{
			setlocale(LC_CTYPE, "Russian");
			int main();
			{
				setlocale(LC_ALL, "rus");
				int a[100][100], N, M, i, j, S = 0, P = 1;
				printf("Введите N и M: ");
				scanf_s("%d %d", &N, &M);
				for (i = 0; i < N; i++)
					for (j = 0; j < M; j++)
					{
						printf("Введите элемент массива: a[%d][%d]: ", i, j);
						scanf_s("%d", &a[i][j]);
					}
				for
					(i = 0; i < N; i++)
					for (j = 0; j < M; j++)
					{
						if ((abs(a[i][j]) < i) && (a[i][j] < 0) && (a[i][j] & 1))
						{
							S = S + a[i][j];
							P = P * a[i][j];
						}
					}
				printf("Сумма =%d", S);
				printf("Произведение =%d", P);
				return 0;
			}
		}
		if (k == 4)
			return 0;
		if (k != 1 && k != 2 && k != 3 && k != 4)
			cout << "Некорректный вариант" << endl;
		cout << "Программу подготовила" << endl << "студентка группы 219/4" << endl << "Марченкова Ксения" << endl << endl;
	}
}

}
