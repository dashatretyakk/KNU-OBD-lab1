База даних Cалону краси складається з двох таблиць: клієнти («Customers») і Послуги  («Orders») із зв’язком один до багатьох.

class Order {
public:
    void setIdOrder(int temp);
    void setIdCustomer(int temp);
    void setIdWorker(int temp);
    void setIdAdmin(int temp);
    void setPrice(int temp);
    void setCost(int temp);
    void setNumberCabinet(int temp);
    void setName(std::string temp);
    void setGroupNameOrders(std::string temp);

   

#include "order.h"
class Customer {
public:
    void setFirstName(std::string temp);
    void setLastName(std::string temp);
    void setSurname(std::string temp);
    void setPhoneNumber(std::string temp);
    void setAddress(std::string temp);
    void setIdCustomer(int temp);

  
(1) Створення клієнтів (getIdCustomer)
(2) Створення послуг (addNewOrder)
(3) Видалення послуг (deleteOrder)
(4) Пошук послуг (printOrders)
