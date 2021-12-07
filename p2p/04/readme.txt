

1. 主题的问题
 不能使用application
 加载布局的时候慎用Application
 -布局
 -字体颜色

2.
  
  最早的启动的是contentProvider


3.

 在aplication里面存储数据是及其愚蠢的


4.
还是ConText的家族

开始胡说了

5.

删除和显示，什么时间使用好，
什么时间使用hide和show
你应该知道了，就看复用与否


6.
跑马灯在xml写获取焦点不可以吗？？？



7.
adapter抽取有必要吗？ 本身带有模板的性质

8.
Viewholder存在的意义没有了

9.

	这个一部的抽取没有见过 ，但是按照业务来说没有影响
    public View getView(int position, View convertView, ViewGroup parent) {
        BaseHolder<T> holder;
        if(convertView == null){
            holder = getHolder();
        }else{
            holder = (BaseHolder<T>) convertView.getTag();
        }

        //装配数据
        T t = list.get(position);
        holder.setData(t);

        return holder.getRootView();
    }

这个写法就是错误的
  @Override
    protected View initView() {
        return View.inflate(UIUtils.getContext(), R.layout.item_product_list, null);
    }
    
    类是多了，但是多了一个无用的类，那个类可以处理一下