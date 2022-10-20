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

    int getIdOrder();
    int getIdCustomer();
    int getIdWorker();
    int getIdAdmin();
    int getPrice();
    int getCost();
    int getNumberCabinet();
    std::string getName();
    std::string getGroupNameOrders();

private:
    int idOrder;
    int idCustomer;
    int idWorker;
    int idAdmin;
    std::string name;
    std::string groupNameOrders;
    int price;
    int cost;
    int numberCabinet;

};


#include "order.h"
class Customer {
public:
    void setFirstName(std::string temp);
    void setLastName(std::string temp);
    void setSurname(std::string temp);
    void setPhoneNumber(std::string temp);
    void setAddress(std::string temp);
    void setIdCustomer(int temp);

    int getIdCustomer();
    std::string getFirstName();
    std::string getLastName();
    std::string getSurname();
    std::string getPhoneNumber();
    std::string getAddress();

    void addNewOrder();
    int getSizeOrderTable(){
        return orders.size();
    }
    void deleteOrder(int deleteValue){
        orders.erase(orders.begin()+deleteValue);
    }
    void printOrders();

private:
    Order createOrder();
    int idCustomer;
    std::string firstName;
    std::string lastName;
    std::string surname;
    std::string phoneNumber;
    std::string address;
    std::vector<Order> orders;
};

(1) Створення клієнтів (getIdCustomer)
(2) Створення послуг (addNewOrder)
(3) Видалення послуг (deleteOrder)
(4) Пошук послуг (printOrders)
