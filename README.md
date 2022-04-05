#include<stdio.h>
#include<string.h>

int main()
{
	char strexp[]="1+2+2+1+2+5+4-1-3+4-8";

	int res=strexp[0]-'0';
	for(int i=1;i<strlen(strexp);i++)
	{
		if(strexp[i]=='+')
		{
        int rightoperand=strexp[i+1]-'0';
		res=res+rightoperand;
		i++;
}
		else if(strexp[i]=='-')
		{
        int rightoperand=strexp[i+1]-'0';
        res=res-rightoperand;
		i++;
		}
	}
	printf("res=%d\n",res);
	return 0;
}
