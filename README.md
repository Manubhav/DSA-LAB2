# DSA-LAB2
## PROGRAM FOR CAESAR CIPHER ENCRYPTION AND DECRYPTION
		#include<stdio.h>
        #include<string.h>
        main()
        {
        char ar[20],i;
        int m,x;
        do
		{
		printf("\nPlease choose following options:\n");
        printf("1 = Encrypt the string.\n");
        printf("2 = Decrypt the string.\n");
        printf("3 = EXIT\n");
        scanf("%d", &x);
        switch(x)
        {
            case 1:
					printf("Enter a Sentence:");    //TAKE INPUT FROM USER
        			scanf("%s",ar);
					for(i=0;i<strlen(ar);i++)
					{
					m=ar[i];
                    if((m>=97&&m<=119)||(m>=65&&m<=87))     //CONDITION FOR ENCRYPTION(a=97 & w=119, A=65 & W=87)
                    {
                        m=m+3;
                        ar[i]=m;
                    }
                    else
                    {
                        m=m-23;
                        ar[i]=m;
                    }
                	}
                    printf("\nCode Language:");
                    puts(ar);
                    break;
            case 2:     
                    printf("Enter a Sentence:");    //TAKE INPUT FROM USER
        			scanf("%s",ar);
					for(i=0;i<strlen(ar);i++)
					{
					m=ar[i];
                    if((m>=100&&m<=122)||(m>=68&&m<=90))     //CONDITION FOR DECRYPTION(d=100 & z=122, D=68 & Z=90)
                    {
                        m=m-3;
                        ar[i]=m;
                    }
                    else
                    {
                        m=m+23;
                        ar[i]=m;
                    }
                	}
					printf("\nCode Language:");
                    puts(ar);
                    break;
			case 3:
					{
						break;
					}
			default:
                {
                    printf("Error");
                }
        }
		}
		while(x!=3);   
        }
