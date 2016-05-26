import urllib.request
import urllib.parse
import sys

url_post = "http://off.aladin.co.kr/usedstore/wsearchresult.aspx?SearchWord=%C1%F6%C5%CA%C7%CF%B4%C2&x=0&y=0"
values = {"OffCode":"suwon"}
params = urllib.parse.urlencode(values)
data = params.encode('utf-8')
print(data)
req = urllib.request.Request(url_post, data)
#req.add_header("Content-Type","application/x-www-form-urlencoded;charset=utf-8")
ft = urllib.request.urlopen(req)

#with ft as response:
#    the_page = response.read()
#print(the_page)

fff=open("search_result2.txt","w")
with ft as response:
	fff.write(response.read().decode('euc-kr'))




#arg = urllib.parse.urlencode(str(sys.argv[1])).encode('utf-8')
arg = "%BF%D3%BD%BC"
url="http://off.aladin.co.kr/usedstore/wsearchresult.aspx?SearchWord="+arg+"&x=0&y=0"
#url="http://off.aladin.co.kr/usedstore/wsearchresult.aspx?SearchWord=%C1%F6%C5%CA%C7%CF%B4%C2&x=0&y=0"



print(url_post)
temp=urllib.request.urlopen(url)
f=open("search_result.txt","w")
#text = temp.read().decode('euc-kr')

text = ft.read().decode('euc-kr')

text2=text[text.find("ss_book_list"):text.find("Search3_Result_SafeBasketArea")].split("<li>")

#f.write(temp.read().decode('euc-kr'))


for i in text2:
#	print (i[i.find("bo_l"):i.find("ss_f_g2")])
	f.write(i[i.find("bo_l"):i.find("ss_f_g2")])

f.close()
temp.close()
