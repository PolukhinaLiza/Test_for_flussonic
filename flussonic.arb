def mas(flu)
  data=flu
  array=[flu]
  i=1
  while i!=5 do
    if data*100%100<=1
      data=data-0.89
    else
      data=data-0.01
    end
    array.unshift(data.round(2))
    i+=1
  end
array
end


def flussonic(paid_till,max_version,min_version)
  paid_till=paid_till.to_s.split('.')
  paid_till=paid_till[2].to_f%100+paid_till[1].to_f/100
  min_version=0 if min_version==nil
  max_version=100 if max_version==nil
  array=mas(FlussonicLastVersion_get)
  find=array.find_all{|elem| elem<=max_version && elem<=paid_till && elem >=min_version}
  if find.empty?
    if max_version == 100
       find=nil
    else
       find=max_version
    end
  end
  return find
end
FlussonicLastVersion_get=20.10 #сделано для удобства вычислений
puts "Список доступных версий лицензии:"
puts flussonic("04.07.2020",20.02,19.01) #вводим любые значения
# FlussonicLastVersion.get=FlussonicLastVersion_get
