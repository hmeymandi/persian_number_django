# persian_number_django
Convert english number to Persian number in django 

########################################################################################

models.py 

class Test (models.Model):
  time=models.DateTimeField()
  
  def persian_number(self):
        persiannumber=str(self.time)
        number={
            '0':'۰',
            '1':'۱',
            '2':'۲',
            '3':'۳',
            '4':'۴',
            '5':'۵',
            '6':'۶',
            '7':'۷',
            '8':'۸',
            '9':'۹',
       }

        for i,j in number.items():
            persiannumber=persiannumber.replace(i,j)
            
        return persiannumber

Template.html
{{persian_number}}

