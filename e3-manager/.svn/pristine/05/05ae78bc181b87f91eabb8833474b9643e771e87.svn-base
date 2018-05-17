package cn.e3mall.controller;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.ResponseBody;

import com.fasterxml.jackson.annotation.JsonFormat.Value;

import cn.e3mall.pojo.TbItem;
import cn.e3mall.service.ItemService;

/**
 * 商品管理
 * @author Administrator
 *
 */
@Controller
public class ItemController {
  
	@Autowired
	private ItemService itemService;
	@RequestMapping("/item/{itemId}")//模板映射
	@ResponseBody //需要有jackson包  如果没有的话 就会报406错误
	public TbItem getItemById(@PathVariable  Long itemId){
		System.out.println(itemId+"SSSSSSSSSSSSSSSSSSSS");
		TbItem tbItem = itemService.getItemById(itemId);
		return tbItem;
	}
	
	
	
}
