namespace ca1
{
    class Program
    {
        static void Main(string[] args)
        {
        }
    }
}
interface IPayable
{
    double GetAmountDue();
    void AddAmountDue(double amount);
    string GetPaymentAddress();
}

class Person
{
    public string Name { get; set; }
}

class Employee : Person, IPayable
{
    public double Salary { get; set; }
    private double _amountDue;
    private string _mailingAddress;

    public void AddAmountDue(double amount)
    {
        _amountDue += amount;
    }

    public double GetAmountDue()
    {
        return _amountDue;
    }

    public string GetPaymentAddress()
    {
        return _mailingAddress;
    }
}
