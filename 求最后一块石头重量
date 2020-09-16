/*求最后一块石头的重量
  有一堆石头,每块石头的重量都是正整数。每一回合,从中选出两块最重的石头,然后将它们一起粉碎。假设石头的重量分别为 x 和 y ,且x<= y 那么粉碎的可能结果如下:
  如果x==y ,那么两块石头都会被完全粉碎;如果x!= y ,那么重量为 x 的石头将会完全粉碎，而重量为y的石头新重量为 y-x 
  最后,最多只会剩下一块石头。返回此石头的重量。
  如果没有石头剩下，就返回0。
/*思路：用递归的方法解决。先将数组从大到小排列，排列后若stones[1]=0,则完成；用stones[0]减去stones[1]，并让stones[1]=0.递归。


/*
  int lastStoneWeight(int* stones, int stonesSize){
    if(stonesSize==1) return stones[0];
    short i,j,tmp;
    for(i=0;i<stonesSize;i++)
        for(j=i+1;j<stonesSize;j++)
            if(stones[j]>stones[i]){
                tmp=stones[j];
                stones[j]=stones[i];
                stones[i]=tmp;
            }
    if(stones[1]==0) return 0;
    stones[0]=stones[0]-stones[1];
    stones[1]=0;
    lastStoneWeight(stones,stonesSize);
    return stones[0];
  }
