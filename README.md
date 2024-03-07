# tasfgsd
#include <iostream.h>
#include <conio.h>

class vecto
{
	int n;
	int *ptr;
	public:
		vecto(int n);
	~vecto();
	void inputvt();
	void sumvt(int *, int *);
	void displayvt(int*);
	void print();
};

vecto::vecto(int n1)
{
	int i;
	n = n1;
	ptr = new int[n1];
	delete[] ptr;
}

void vecto::inputvt()
{
	int i;
	cout << "\n input vecto:";
	for (i = 0; i < n; i++)
	{
		cout << "ptu[" << i << "]=";
		cin >> ptr[i];
	}
}

void vecto::displayvt(int *p)
{
	int i;
	for (i = 0; i < n; i++) p[i] = ptr[i];
}

void vecto::print()
{
	int i;
	for (i = 0; i < n; i++)
	{
		cout << ptr[i] << " ";
		cout << "\n";
	}
}

void vecto::sumvt(int *p, int *p1)
{
	int i;
	for (i = 0; i < n; i++) ptr[i] = p[i] + p1[i];
}

void main()
{
	int n, *p, *p1;
	clrscr();
	cout << "enter sign of vecto :" << '\n';
	cout << "n=";
	cin >> n;
	vecto a(n), b(n), c(n);
	cout << "input vecto a:" << endl;
	a.inputvt();
	cout << "input vecto b:" << endl;
	b.inputvt();
	a.displayvt(p);
	b.displayvt(p1);
	b.print();
	cout << "\n display vecto tong c" << endl;
	c.print();
	getch();
}
