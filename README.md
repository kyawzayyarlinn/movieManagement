# movieManagemepublic class autoboxing_unboxing
{
	public static void main(String[] args)
	{
		long startTime,endtime;
		startTime = System.currentTimeMillis();
		Integer i=0;
	    while(i<5000000)
		{
			i++;
		}
		endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
		startTime=System.currentTimeMillis();
		int ii=0;
		while(ii<5000000)
		{
			ii++;
		}
		endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
	}
}public class string_same_length
{
	public static void main(String[] args)
	{
		long startTime,endtime;
		startTime = System.currentTimeMillis();
		String a="abc";
		String b="def";
		for(int i=0;i<1000000;i++)
		{
			if(a.equalsIgnoreCase(b))
			{

			}
		}
	    endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
		startTime=System.currentTimeMillis();
		String c="abc";
		String d="def";
		for(int i=0;i<1000000;i++)
		{
			if(c.equals(d))
			{

			}
		}
		endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
	}
}public class string_different_length
{
	public static void main(String[] args)
	{
		long startTime,endtime;
		startTime = System.currentTimeMillis();
		String a="abc";
		String b="defg";
		for(int i=0;i<1000000;i++)
		{
			if(a.equalsIgnoreCase(b))
			{

			}
		}
	    endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
		startTime=System.currentTimeMillis();
		String c="abc";
		String d="defg";
		for(int i=0;i<1000000;i++)
		{
			if(c.equals(d))
			{

			}
		}
		endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
	}
}public class string_comparison
{
	public static void main(String[] args)
	{
		long startTime,endtime;
		startTime = System.currentTimeMillis();
		String name="abc";
		for(int i=0;i<1000000;i++)
		{
			if(name!=null && name.equals(""))
				{
				
			}
		}
	    endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
		startTime=System.currentTimeMillis();
		String name2="abc";
		for(int i=0;i<1000000;i++)
		{
			if(name2!=null && name2.length()==0)
			{

			}
		}
		endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
	}public class runtime_string_initialization
{
	public static void main(String[] args)
	{
		long startTime,endtime;
		startTime = System.currentTimeMillis();
		String name="abc";
		for(int i=0;i<100000;i++)
		{
			String x= "Hello";
			x+=",";
			x+="Mr.";
			x+=name;
		}
		endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
		startTime=System.currentTimeMillis();
		String name2="abc";
		for(int i=0;i<100000;i++)
		{
			String x= (new StringBuffer()).append("Hello").append(",").append("Mr.").append(name2).toString();
		}
		endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
	}
}public class intern_string
{
	public static void main(String[] args)
	{
		long startTime,endtime;
		startTime = System.currentTimeMillis();
		String a=new String("abc").intern();
		String b=new String("abc").intern();
		for(int i=0;i<1000000;i++)
		{
			if(a.equals(b))
			{

			}
		}
	    endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
		startTime=System.currentTimeMillis();
		String c=new String("abc").intern();
		String d=new String("abc").intern();
		for(int i=0;i<1000000;i++)
		{
			if(c == d)
			{

			}
		}
		endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
	}public class compile_time_initialization
{
	public static void main(String[] args)
	{
		long startTime,endtime;
		startTime = System.currentTimeMillis();
		for(int i=0;i<100000;i++)
		{
			String x= "Hello"+","+" "+"World";
		}
		endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
		startTime=System.currentTimeMillis();
		for(int i=0;i<100000;i++)
		{
			String x= new String("Hello"+","+" "+"World");
		}
		endtime= System.currentTimeMillis();
		System.out.println(endtime-startTime);
	}
}
}
}

