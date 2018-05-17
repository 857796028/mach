package cn.e3mall.service.impl;

import java.util.List;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

import cn.e3mall.mapper.TbItemMapper;
import cn.e3mall.mapper.TbItemParamMapper;
import cn.e3mall.pojo.TbItem;
import cn.e3mall.pojo.TbItemExample;
import cn.e3mall.pojo.TbItemExample.Criteria;
import cn.e3mall.service.ItemService;
/**
 * 端口管理Service
 * @author Administrator
 *
 */
@Service
public class ItemServiceImpl implements ItemService{
    @Autowired
    private TbItemMapper itemMapper;
	
	public TbItem getItemById(Long itemId) {
		
		//查询方式1：
		//TbItem tbItem = itemMapper.selectByPrimaryKey(itemId);  根据主键查询 
		
		
		System.out.println("ServiceImpl传来的itemId为："+itemId);
		//设置查询条件
		
		TbItemExample example = new TbItemExample();
		Criteria criteria = example.createCriteria();
		//设置查询条件
		criteria.andIdEqualTo(itemId);
        //执行查询
		List<TbItem> list = itemMapper.selectByExample(example); //得到商品列表
		if(list != null && list.size() >0 ){
		  System.out.println(list.get(0));
		return list.get(0);
		}
		return null;
		
	}

}
