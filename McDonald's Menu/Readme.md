# Nutritional Facts of McDonalds Menu

<img src="https://raw.githubusercontent.com/mohan-gupta/EDA/main/McDonald's%20Menu/Plots/McDonalds.webp" width="1000" height="600"><br><br>

<b>In The Notebook you will find Exploration of McDonald's Menu, I have picked this data from Kaggle and<br>
I have tried to answer some of the questions mentioned with this dataset.</b><br>

## Context
Ray Kroc wanted to build a restaurant system that would be famous for providing food of consistently high quality and uniform methods of preparation.<br>
He wanted to serve burgers, buns, fries and beverages that tasted just the same in Alaska as they did in Alabama. To achieve this, he chose a unique path:<br>
persuading both franchisees and suppliers to buy into his vision, working not for McDonald’s but for themselves, together with McDonald’s. Many of McDonald’s<br>
most famous menu items – like the Big Mac, Filet-O-Fish, and Egg McMuffin – were created by franchisees.<br>
Link to the [dataset](https://www.kaggle.com/mcdonalds/nutrition-facts).<br>
Here are some of the facts that I discovered:<br>

Data Distribution
<img src ="https://github.com/Mohan-Gupta/EDA/blob/main/McDonald's%20Menu/Plots/datadist.png">
<br><br>

<img src="https://github.com/Mohan-Gupta/EDA/blob/main/McDonald's%20Menu/Plots/CategoryPie.png">
<p>Hence, it can be observed that most of the McDonald's menu is occupied by Coffe&Tea then by Breakfast with a contribution of 36.5% and 16.2% respectively.<br>
Smoothies-Shakes, Chiken-Fish and Beverages contibuting around 10% each.</p><br><br>

<img src="https://github.com/Mohan-Gupta/EDA/blob/main/McDonald's%20Menu/Plots/Corr_hearmap.png">
<p>There exist Strong correlation of Calories with Fat, Cholestrol, Sodium, Carbohydrates, Protein and Iron<br> With pearson correlation ranging between 0.65-0.90<br>
Therefore, meals with high calories will also have high Fat (both Saturated and Trans), Cholestrol, Sodium, Carbohydrates, Protein and Iron.<br>
Sodium and Sugar are negatively correlated meaning meals with high Sugar may have low amount of Sodium and vice-versa.</p><br><br>

<img src="https://github.com/Mohan-Gupta/EDA/blob/main/McDonald's%20Menu/Plots/CalsDist.png">
<p>Beverages and Desserts have lowest range of calories,<br>
whereas Smoothies&Shakes and Breakfast have highest range of Calories.<br>
Also, In Breakfast category there are meals ranging between 990-1150 calories.<br>
Although breakfast and Smoothies&Shakes have highest range however,<br>
the meal with maximum calories in McDonald's menu lies in the Chicken&Fish category with 1880 Calories.</p><br><br>

<img src="https://github.com/Mohan-Gupta/EDA/blob/main/McDonald's%20Menu/Plots/CholsDist.png">
<p>Meals with High Cholestrol are mainly from the Breakfast Category in the McDonald's menu,<br>
Apart From Breakfast all other categories have low cholestrols with minimum in beverages.<br><br>
  
<img src="https://github.com/Mohan-Gupta/EDA/blob/main/McDonald's%20Menu/Plots/SugarDist.png">
<p>Categories Like Desserts, Beverages,Coffe&Tea and Smoothies&Shakes have high Sugar Meals<br>
with highest in Smoothies and Shakes.<br>
While all other categories have very low sugar compared to them</p><br><br>

<img src="https://github.com/Mohan-Gupta/EDA/blob/main/McDonald's%20Menu/Plots/AvgCals.png">
<br><br>

<img src="https://github.com/Mohan-Gupta/EDA/blob/main/McDonald's%20Menu/Plots/bevgCals.png">
<p>In beverages, Sprite(Large), Dr.Pepper(Large),Coca-Cola Classic(Large) have the maximum claories,<br>
while all the diet drinks have 0 calorie.</p><br><br>
  
 <img src="https://github.com/Mohan-Gupta/EDA/blob/main/McDonald's%20Menu/Plots/GrilledVsCrispy.png">
<p>Takeaways from the above plot,<br>
Grilled Chicken Sandwich is more healthy than the crispy chicken sandwich.<br>
It has less Calories, less Fats, more Vitamins, more Protein and more Calcium and Iron<br>
However, Grilled Chicken Sandwich has more cholesterol than the Crispy one.
</p><br><br>

<img src="https://github.com/Mohan-Gupta/EDA/blob/main/McDonald's%20Menu/Plots/WholeVsWhite.png">
<p>Observations From the above plot: <br>
    It is hard to differentiate between which one is more healthier.<br>
    While Egg Whites have more Calories but they have less Cholesterol and less Trans Fat.<br>
    Whereas Whole Eggs have more Cholesterol but they have more Vitamins, Calcium and Iron.</p><br><br>
    
 <b>If you Liked my work then do give this repo a star.
