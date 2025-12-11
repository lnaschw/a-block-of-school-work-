# a-block-of-school-work-
#include "stm32f10x.h"
#include "delay.h"
#include "PWM.h"

int main(void)
{
	Delay_Init();
	
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOB, ENABLE);
	
	GPIO_InitTypeDef GPIO_InitStructB12;
	GPIO_InitStructB12.GPIO_Pin = GPIO_Pin_12;
	GPIO_InitStructB12.GPIO_Mode = GPIO_Mode_IPD;
	GPIO_InitStructB12.GPIO_Speed = GPIO_Speed_2MHz;
	GPIO_Init(GPIOB, &GPIO_InitStructB12);
	
	
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOB, ENABLE);
	GPIO_InitTypeDef GPIO_InitStructB13;
	GPIO_InitStructB13.GPIO_Pin = GPIO_Pin_13;
	GPIO_InitStructB13.GPIO_Mode = GPIO_Mode_IPD;
	GPIO_InitStructB13.GPIO_Speed = GPIO_Speed_2MHz;
	GPIO_Init(GPIOB, &GPIO_InitStructB13);
	
	
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOB, ENABLE);
	
	GPIO_InitTypeDef GPIO_InitStructB14;
	
	GPIO_InitStructB14.GPIO_Pin = GPIO_Pin_14;
	GPIO_InitStructB14.GPIO_Mode = GPIO_Mode_IPD;
	GPIO_InitStructB14.GPIO_Speed = GPIO_Speed_2MHz;
	GPIO_Init(GPIOB, &GPIO_InitStructB14);
	
	
	
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOB, ENABLE);
	GPIO_InitTypeDef GPIO_InitStructB15;
	
	GPIO_InitStructB15.GPIO_Pin = GPIO_Pin_15;
	GPIO_InitStructB15.GPIO_Mode = GPIO_Mode_IPD;
	GPIO_InitStructB15.GPIO_Speed = GPIO_Speed_2MHz;
	GPIO_Init(GPIOB, &GPIO_InitStructB15);
	
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA, ENABLE);
	
	GPIO_InitTypeDef GPIO_InitStructA8;
	
	GPIO_InitStructA8.GPIO_Pin = GPIO_Pin_8;
	GPIO_InitStructA8.GPIO_Mode = GPIO_Mode_IPD;
	GPIO_InitStructA8.GPIO_Speed = GPIO_Speed_2MHz;
	GPIO_Init(GPIOA, &GPIO_InitStructA8);
	
	
	
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA, ENABLE);
		GPIO_InitTypeDef GPIO_InitStructA9;
	
	GPIO_InitStructA9.GPIO_Pin = GPIO_Pin_9;
	GPIO_InitStructA9.GPIO_Mode = GPIO_Mode_IPD;
	GPIO_InitStructA9.GPIO_Speed = GPIO_Speed_2MHz;
	GPIO_Init(GPIOA, &GPIO_InitStructA9);
	
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA, ENABLE);
	
	GPIO_InitTypeDef GPIO_InitStructA10;
	
	GPIO_InitStructA10.GPIO_Pin = GPIO_Pin_10;
	GPIO_InitStructA10.GPIO_Mode = GPIO_Mode_IPD;
	GPIO_InitStructA10.GPIO_Speed = GPIO_Speed_2MHz;
	GPIO_Init(GPIOA, &GPIO_InitStructA10);
	
	
	
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA, ENABLE);
	GPIO_InitTypeDef GPIO_InitStructA11;
	GPIO_InitStructA11.GPIO_Pin = GPIO_Pin_11;
	GPIO_InitStructA11.GPIO_Mode = GPIO_Mode_IPD;
	GPIO_InitStructA11.GPIO_Speed = GPIO_Speed_2MHz;
	GPIO_Init(GPIOA, &GPIO_InitStructA11);
	
	//uint16_t  yuan=0;
	
		
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA, ENABLE);
	
	GPIO_InitTypeDef GPIO_InitStructA2;
	
	GPIO_InitStructA2.GPIO_Pin = GPIO_Pin_2;
	GPIO_InitStructA2.GPIO_Mode = GPIO_Mode_Out_PP;
	GPIO_InitStructA2.GPIO_Speed = GPIO_Speed_2MHz;
	GPIO_Init(GPIOA, &GPIO_InitStructA2);
	
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA, ENABLE);
	
	GPIO_InitTypeDef GPIO_InitStructA3;
	
	GPIO_InitStructA3.GPIO_Pin = GPIO_Pin_3;
	GPIO_InitStructA3.GPIO_Mode = GPIO_Mode_Out_PP;
	GPIO_InitStructA3.GPIO_Speed = GPIO_Speed_2MHz;
	GPIO_Init(GPIOA, &GPIO_InitStructA3);
	
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA, ENABLE);
	
	GPIO_InitTypeDef GPIO_InitStructA4;
	
	GPIO_InitStructA4.GPIO_Pin = GPIO_Pin_4;
	GPIO_InitStructA4.GPIO_Mode = GPIO_Mode_Out_PP;
	GPIO_InitStructA4.GPIO_Speed = GPIO_Speed_2MHz;
	GPIO_Init(GPIOA, &GPIO_InitStructA4);
	
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA, ENABLE);
	
	GPIO_InitTypeDef GPIO_InitStructA5;
	
	GPIO_InitStructA5.GPIO_Pin = GPIO_Pin_5;
	GPIO_InitStructA5.GPIO_Mode = GPIO_Mode_Out_PP;
	GPIO_InitStructA5.GPIO_Speed = GPIO_Speed_2MHz;
	GPIO_Init(GPIOA, &GPIO_InitStructA5);
	PWM_Init_left();
	PWM_Init_right();
	// shi neng gpio b12-15 A8-11,bing qie she zhi wei xia la shu ru mo shi 
	while(1)
{
	
uint16_t pin_state_B12 = (GPIO_ReadInputDataBit(GPIOB, GPIO_Pin_12) == Bit_SET) ? 1 : 0;
uint16_t pin_state_B13 = (GPIO_ReadInputDataBit(GPIOB, GPIO_Pin_13) == Bit_SET) ? 1 : 0;
uint16_t pin_state_B14 = (GPIO_ReadInputDataBit(GPIOB, GPIO_Pin_14) == Bit_SET) ? 1 : 0;
uint16_t pin_state_B15 = (GPIO_ReadInputDataBit(GPIOB, GPIO_Pin_15) == Bit_SET) ? 1 : 0;

uint16_t pin_state_A8 = (GPIO_ReadInputDataBit(GPIOA, GPIO_Pin_8) == Bit_SET) ? 1 : 0;
uint16_t pin_state_A9 = (GPIO_ReadInputDataBit(GPIOA, GPIO_Pin_9) == Bit_SET) ? 1 : 0;
uint16_t pin_state_A10 = (GPIO_ReadInputDataBit(GPIOA, GPIO_Pin_10) == Bit_SET) ? 1 : 0;
uint16_t pin_state_A11 = (GPIO_ReadInputDataBit(GPIOA, GPIO_Pin_11) == Bit_SET) ? 1 : 0;

// du qu hong wai ba kou shu ju zhuang tai  	

	int16_t left = pin_state_B12*2+pin_state_B13*2+pin_state_B14+pin_state_B15;
	int16_t right = pin_state_A8+pin_state_A9+pin_state_A10*2+pin_state_A11*2;
// yin wei che tiao guo yi ci qian hou , suo yi zuo you shi fan de !!! 			 
/*PWM_Init_right();
	PWM_SetCompare1_right(20);			 
   PWM_Init_left();
   PWM_SetCompare1_left(20);
	GPIO_SetBits(GPIOA,GPIO_Pin_2);//zuo 
	GPIO_SetBits(GPIOA,GPIO_Pin_4);//you 
	GPIO_ResetBits(GPIOA,GPIO_Pin_3);//zuo 
  GPIO_ResetBits(GPIOA,GPIO_Pin_5);//you 
*/

/*
GPIO_SetBits(GPIOA,GPIO_Pin_2);//zuo 
	GPIO_SetBits(GPIOA,GPIO_Pin_4);//you 
	GPIO_ResetBits(GPIOA,GPIO_Pin_3);//zuo 
  GPIO_ResetBits(GPIOA,GPIO_Pin_5);//you 
PWM_Init_left();
    for(int i = 100; i >= 0; i -= 10) {
        PWM_SetCompare1_left(i);
        Delay(500);
    }
PWM_SetCompare1_left(0);
PWM_Init_right();
    for(int i = 100; i >= 0; i -= 10) {
        PWM_SetCompare1_right(i);
        Delay(500);
    }
PWM_SetCompare1_right(0);
	*/


				
if (left==right)
	{
				PWM_SetCompare1_left(25);
			  PWM_SetCompare1_right(25);
				GPIO_SetBits(GPIOA,GPIO_Pin_2);
				GPIO_ResetBits(GPIOA,GPIO_Pin_3);
				GPIO_SetBits(GPIOA,GPIO_Pin_4); 
				GPIO_ResetBits(GPIOA,GPIO_Pin_5);
				
			 Delay(50);
	}
	
	/*if (pin_state_A11==1&&pin_state_A10==0)
  {    
		yuan++;
	}
	if (pin_state_B12==1&&pin_state_B13==0)
  {    
		yuan++;
	}
	if (yuan==2)
	{
			PWM_SetCompare1_left(10);
			PWM_SetCompare1_right(30);
			GPIO_SetBits(GPIOA,GPIO_Pin_2);
			GPIO_SetBits(GPIOA,GPIO_Pin_4);
			Delay(10);
	}*/
	   switch(left-right)
		 {
      case 6:for(int i = 0; i < 50 ;i++)
							{
								Delay(1);
								PWM_SetCompare1_left(0);
			          PWM_SetCompare1_right(60);
							  GPIO_SetBits(GPIOA,GPIO_Pin_2);
			          GPIO_ResetBits(GPIOA,GPIO_Pin_3);
						  	GPIO_SetBits(GPIOA,GPIO_Pin_4);
						  	GPIO_ResetBits(GPIOA,GPIO_Pin_5);
							}
							break;
			 case 5:for(int i = 0; i < 50 ;i++)
							{
							Delay(1);
							PWM_SetCompare1_left(10);
			        PWM_SetCompare1_right(45);
							GPIO_SetBits(GPIOA,GPIO_Pin_2);
							GPIO_ResetBits(GPIOA,GPIO_Pin_3);
							GPIO_SetBits(GPIOA,GPIO_Pin_4);
							GPIO_ResetBits(GPIOA,GPIO_Pin_5);
							break;
							}
			 case 4:for(int i = 0; i < 25 ;i++)
							{
							Delay(1);
							PWM_SetCompare1_left(12);
			        PWM_SetCompare1_right(40);
							GPIO_SetBits(GPIOA,GPIO_Pin_2);
							GPIO_ResetBits(GPIOA,GPIO_Pin_3);
							GPIO_SetBits(GPIOA,GPIO_Pin_4);
							GPIO_ResetBits(GPIOA,GPIO_Pin_5);
							}
							break;
			 case 3:for(int i = 0; i < 25 ;i++)
							{
							Delay(1);
							PWM_SetCompare1_left(15);
			        PWM_SetCompare1_right(25);
							GPIO_SetBits(GPIOA,GPIO_Pin_2);
							GPIO_ResetBits(GPIOA,GPIO_Pin_3);
							GPIO_SetBits(GPIOA,GPIO_Pin_4);
							GPIO_ResetBits(GPIOA,GPIO_Pin_5);
							}
							break;
			 case 2:for(int i = 0; i < 25 ;i++)
							{
							Delay(1);
							PWM_SetCompare1_left(15);
			        PWM_SetCompare1_right(25);
							GPIO_SetBits(GPIOA,GPIO_Pin_2);
							GPIO_ResetBits(GPIOA,GPIO_Pin_3);
							GPIO_SetBits(GPIOA,GPIO_Pin_4);
							GPIO_ResetBits(GPIOA,GPIO_Pin_5);
							}
							break;
		   case 1:for(int i = 0; i < 25 ;i++)
							{
							Delay(1);
							PWM_SetCompare1_left(25);
			        PWM_SetCompare1_right(25);
							GPIO_SetBits(GPIOA,GPIO_Pin_2);
							GPIO_ResetBits(GPIOA,GPIO_Pin_3);
							GPIO_SetBits(GPIOA,GPIO_Pin_4); 
							GPIO_ResetBits(GPIOA,GPIO_Pin_5);
							Delay(50);
							}
							break;
			 case -1:for(int i = 0; i < 25 ;i++)
							{
							Delay(1);
							PWM_SetCompare1_left(25);
			        PWM_SetCompare1_right(25);
							GPIO_SetBits(GPIOA,GPIO_Pin_2);
							GPIO_ResetBits(GPIOA,GPIO_Pin_3);
							GPIO_SetBits(GPIOA,GPIO_Pin_4);
							GPIO_ResetBits(GPIOA,GPIO_Pin_5);
							}
							break;
		   case -2:for(int i = 0; i < 25 ;i++)
							{
							Delay(1);
							PWM_SetCompare1_left(25);
			        PWM_SetCompare1_right(15);
							GPIO_SetBits(GPIOA,GPIO_Pin_2);
							GPIO_ResetBits(GPIOA,GPIO_Pin_3);
							GPIO_SetBits(GPIOA,GPIO_Pin_4);
							GPIO_ResetBits(GPIOA,GPIO_Pin_5);
							}
							break;
	     case -3:for(int i = 0; i < 25 ;i++)
							{
							Delay(1);
							PWM_SetCompare1_left(25);
			        PWM_SetCompare1_right(15);
							GPIO_SetBits(GPIOA,GPIO_Pin_2);
							GPIO_ResetBits(GPIOA,GPIO_Pin_3);
							GPIO_SetBits(GPIOA,GPIO_Pin_4);
							GPIO_ResetBits(GPIOA,GPIO_Pin_5);
							}
							break;
			 case -4:for(int i = 0; i < 25 ;i++)
							{
							Delay(1);
							PWM_SetCompare1_left(40);
			        PWM_SetCompare1_right(12);
							GPIO_SetBits(GPIOA,GPIO_Pin_2);
							GPIO_ResetBits(GPIOA,GPIO_Pin_3);
							GPIO_SetBits(GPIOA,GPIO_Pin_4);
							GPIO_ResetBits(GPIOA,GPIO_Pin_5);
 							break;
			 case -5:for(int i = 0; i < 50 ;i++)
							{
							Delay(1);
							PWM_SetCompare1_left(45);
			        PWM_SetCompare1_right(10);
							GPIO_SetBits(GPIOA,GPIO_Pin_2);
							GPIO_ResetBits(GPIOA,GPIO_Pin_3);
							GPIO_SetBits(GPIOA,GPIO_Pin_4);
							GPIO_ResetBits(GPIOA,GPIO_Pin_5);
   						}
							break;
			 case -6:for(int i = 0; i < 75 ;i++)
							{
							Delay(1);
							PWM_SetCompare1_left(60);
			        PWM_SetCompare1_right(0);
							GPIO_SetBits(GPIOA,GPIO_Pin_2);
							GPIO_ResetBits(GPIOA,GPIO_Pin_3);
							GPIO_SetBits(GPIOA,GPIO_Pin_4);
							GPIO_ResetBits(GPIOA,GPIO_Pin_5);
					    }
							break;
}}}}		 
