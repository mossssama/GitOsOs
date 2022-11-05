GitOsOs <a name="TOP"></a>
===================
# **Git Commands**
1. DataFlow
2. Information
3. Configuration
4. Security

- - - - 
## **1. Data Flow **
### 1.1 Forward
### 1.2 BackWard
### 1.3 Branching
### 1.4 Merging
### 1.5 Stashing
### 1.6 Tagging/Releasing

### 1.1 Forward 
1.1.1 Initalize a repo in working directory (used when we create repo from scratch)
    
    git init

<br/><br/>
1.1.2 Add a file/fileUpdate from working directory to staging area
Use git add <fileName> as the following three examples

    git add OsOs.txt
    
    git add ProjectDirectory
    
    git add *
    
<br/><br/>
1.1.3 Add all files at staging area to local repo
Use git commit -m <"str"> 

    git commit -m "Adding BroadCast Receiver to Project"
    
<br/><br/>
1.1.4 Add all files at local repo to remote repo;push only
Use git push <remoteRepoName> <localRepoName/tagName>   
    
    git push origin main
    
    git push origin master
    
<br/><br/>
1.1.5 Add all files at local repo to remote repo;pull then push
Use git push -u <remoteRepoName> <localRepoName/tagName>
    
    git push -u origin main
    
    git push -u origin master
    
<br/><br/>
1.1.6 Add project to remote repo with this name 
Use git remote add <remoteRepoName> <https> 
    
    git remote add main https://github.com/mossssama/GitOsOs/
    
<br/><br/>





## 2. Information 
**SQLite : is database used to store data localy & permenantly using CRUD operations in SQL language**

[1] Write the following inside the class you want to use SQLiteDatabase in it

    DBHelper dbHelper=new DBHelper(getApplicationContext());
    ClassModel recordOne = new ClassModel(clmOneData,clmTwoData);
<br/><br/>
[2] Use classModel instances as an input parameters to the SQLite DBHelper

    ClassModel recordOne = new ClassModel(clmOneData,clmTwoData);
    dbHelper.addRecord(recordOne);
    
OR    
   
    dbHelper.addRecord(new ClassModel(clmOneData,clmTwoData));
<br/><br/>
[3] Use any function inside DBHelper using dbHelper instance

    dbHelper.getColumn(1);
    
and so on

<br/><br/>
# 3. Configuration #
**RecyclerView : ViewGroup contains views corresponding to our data**
**RecyclerViewAdapter : Adapter binds data from dataSet to Views that are displayed inside RecyclerView 

[1] Add a recyclerView widget to the xml file of an activity
    for example activity_main.xml

    <androidx.recyclerview.widget.RecyclerView
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:id="@+id/rv"
        app:layout_constraintBottom_toTopOf="@+id/button4"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
<br/><br/>
[2] Create an xml layout to specify the how will each item in the recycler View will look like
    for example create recyclerview_item.xml and add this to it; we assume item contains only textView

    <?xml version="1.0" encoding="utf-8"?>
    <LinearLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        android:padding="10dp">

        <TextView
            android:id="@+id/textViewID"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textSize="20sp"/>

    </LinearLayout>
<br/><br/>
[3] Add the RecyclerView Adapter class to your project directory

<br/><br/>
**At the class which it's layout contains the recyclerView widget; do number 4,5,6**
<br><br/>
[4] Add the following function to the class which it's layout contains the recyclerView widget
    Here in our example is MainActivity.class

    public static RecyclerViewAdapter adapter;
    public void recyclerViewInit(ArrayList dataSource, RecyclerView rv, Context context,RecyclerViewAdapter.ItemClickListener click){
        // set up the RecyclerView
        rv.setLayoutManager(new LinearLayoutManager(context));
        adapter = new RecyclerViewAdapter(context, dataSource);
        adapter.setClickListener(click);
        rv.setAdapter(adapter);
    }
    
<br/><br/>
[5] Put the data you want to fill the recyclerView with in an array; 
    Hint: here we used the array as the dataSource in the previous recyclerViewInit function
    
[5.1] Populate using an array directly

    ArrayList arr = new ArrayList<String>();
    arr.add("Horse");   arr.add("Cow"); arr.add("Camel");   arr.add("Sheep");   arr.add("Goat");
    arr.add("Horse");   arr.add("Cow"); arr.add("Camel");   arr.add("Sheep");
         
OR  
    
[5.2] Using SharedPrefs
    
    SharedPrefSingleton.init(getApplicationContext());
    SharedPrefSingleton.write("0","Horse"); SharedPrefSingleton.write("1","Cow");   SharedPrefSingleton.write("2","Camel");
    SharedPrefSingleton.write("3","Sheep"); SharedPrefSingleton.write("4","Goat");  SharedPrefSingleton.write("5","Horse");
    ArrayList arr = SharedPrefSingleton.readAll();

OR  
    
[5.3] return all rows from database inform of array; previous SQLite class contains returning rows inform of array
    
    DBHelper dbHelper=new DBHelper(getApplicationContext());
    dbHelper.addRecord(new ClassModel(1,"mohamed"));
    dbHelper.addRecord(new ClassModel(2,"m"));
    dbHelper.addRecord(new ClassModel(3,"messi"));
    ArrayList arr = dbHelper.getColumn(1);

<br/><br/>
[6]. Call the recyclerViewInit function
    
    recyclerViewInit(arr,findViewById(R.id.rv),getApplicationContext(),this);
    
    
<br/><br/>
# To Be Continued #

    Stay Tuned

