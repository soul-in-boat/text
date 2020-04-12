1
#coding:gbk
"""
程序目标：通过调用函数实现RPSLS游戏
作者：迟焕龙
日期：2020/04/07
"""
# 0 - 石头
# 1 - 史波克 
# 2 - 纸
# 3 - 蜥蜴
# 4 - 剪刀
import random
computer_guess=random.randint(0,4)#产生随机数
num=computer_guess#赋值
def RPSLS(a,b):#自定义函数
	while a==1:
		if b=="蜥蜴":
			print("计算机的选择为：史波克")
			print("您赢了！")
		break
	while a==0:
		if b=="布":
			print("计算机的选择为：石头")
			print("您赢了")
		if b=="史波克":
			print("计算机的选择为：石头")
			print("机器赢了！")
		if b=="剪刀":
			print("计算机的选择为：石头")
			print("机器赢了！")
		break
	while a==2:
		print("计算机的选择为：布")
		if b=="剪刀":
			print("您赢了!")
		if b=="石头":
			print("机器赢了！")
		break
	while a==3:
		print("计算机的选择为：蜥蜴")
		if b=="石头":
			print("您赢了！")
		if b=="史波克":
			print("机器赢了！")
		break
	while a==4:
		print("计算机的选择为：剪刀")
		if b=="布":
			print("机器赢了！")
		if b=="石头":
			print("您赢了！")
		break				
print("请输入您的选择:")
guess=str(input())
name=set(['石头','剪刀','布','蜥蜴','史波克'])
print("--------")
if guess not in name:#验证
	print("Error: No Correct Name.")
if guess in name:#调用函数
	compare=RPSLS(num,guess)

