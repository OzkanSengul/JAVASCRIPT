#include <stdio.h>
#include <unistd.h>
#include <stdio.h>
#include <string.h>
#include <sys/mman.h>
#include <unistd.h>

int InitMyMalloc (int YıgınBoyutu){
	int* Girilendeger;
	printf("Lutfen 4096 veya 4096 sayisinin katlarini giriniz;\n");
	scanf("%d",Girilendeger);
	int** deger=strcmp (Girilendeger,"\n"==0);

		if (deger==0)
		{
		YıgınBoyutu=4096; /* code */
		}
		else{	
	size_t pagesize=getpagesize();
	printf("%zu\n",pagesize);
	YıgınBoyutu=pagesize*Girilendeger;}
	return YıgınBoyutu;
	/*char * region = mmap(
    (void*) (YıgınBoyutu * (1 << 2)),   // Map from the start of the 2^20th page
    YıgınBoyutu,                         // for one page length
    PROT_READ|PROT_WRITE|PROT_EXEC,
    MAP_ANON|MAP_PRIVATE,             // to a private block of hardware memory
    0,
    0
 	 );
  if (region == MAP_FAILED) {
    perror("Could not mmap");
    return 1;
  }*/
}
int main(void) {
	int x;
	x=InitMyMalloc(x);
 	printf("%d",x);

return 0;
}
