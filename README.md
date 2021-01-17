# leetcode-.github.io
leetcode刷题记录
第一题

    bool ListDeletemin(SqList &L,int e)//删除元素并用最后一个补上
    {
        if(L.length==0)
            return false;
        e=L.data[0];
        int pos=0;
        for(int i=1;i<L.length;i++)
        {
            if(e>L.data[i])
            {
                e=L.data[i];
                pos=i;
            }
        }
        L.data[pos]=L.data[L.length-1];
        L.length--;
        return true;
    }

第二题

    void Reserve(SqList &L){//逆置L所有元素
        int temp;
        for(i=0;i<L.length;i++){
            temp=L.data[i];
            L.data[i]=L.data[L.length-i-1];
            L.data[L.length-i-1]=temp;
        }
    }

第三题 删除表中值为x的元素

    void del_x(Sqlist &L,int x){
        int k;
        for(i=0;i<L.length;i++)
        {
            if(L.data[i]!=x)
            {
                L.data[k]=L.data[i];
                k++;
            }
        }
        L.length=k;//
    }

第四题 删除值s与t之间的所有元素

    void del(SqList &L,int s,int t){
        int i,j;
        if(s>=t||L.length=0)
            return false;
        for(i=0;i<L.length&&L.data[i]<s;i++)
        {
            if(i>=L.length)
            {
                return false;
            }
        }
        
        for(j=i;j<L.length&&L.data[j]<=t;j++)//寻找值大于t的第一个元素   
        for(;j<L.length;i++,j++)
            {
                L.data[i]=L.data[j];
            }      
        L.length=i;
        return true;
    }














