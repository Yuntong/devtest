# devtest
#1

#2
class StudentsMark(models.Model):
    subjects = models.CharField(max_length=20)
    teachers = models.CharField(max_length=20)
    students = models.CharField(max_length=20)
    classes = models.IntField(max_length=2)
    grade = models.IntField(max_length=3)
    results = models.IntField(max_length=3)

class log(models.Model):
    times = models.DateTimeField(default=timezone.now)
    subjects = models.CharField(max_length=20)




def jia(request):
    transcript = get(Myarticle,pk=request)
    return transcript

def yi(request):
    log = get(log,pk=request)
    return log




#3 根据log的时间戳 将现在的时间和上次查询的时间取绝对值 
 #if value < 1min  return

#4 判断当前用户id 是否等于 查询用户的id

