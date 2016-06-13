#sql 更新
··· sql

update Product set new_patterndepth=substring(new_patterndepth,2,len(new_patterndepth)-1) where new_patterndepth is not null and isnumeric(new_patterndepth)<>1 and new_patterndepth not like '%MM'

update Product set new_patterndepth=substring(new_patterndepth,0,charindex('MM',new_patterndepth,0))  where new_patterndepth is not null and isnumeric(new_patterndepth)<>1 and new_patterndepth like '%MM'
···