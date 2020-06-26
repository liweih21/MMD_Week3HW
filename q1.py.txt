#fn
def pv_calc(future_value, years, inflation_rate):
    present_value = [future_value]
    for i in range(1,years,1):
        present_value.append(present_value[i-1]/ (1 + inflation_rate))
    return present_value[::-1]

#run a sample
pv_calc(10000, 5, 0.075)