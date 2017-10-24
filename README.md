using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;

namespace Method
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
        }

        private void buttonplus_Click(object sender, RoutedEventArgs e)
        {
           
            addup(int.Parse(textBox.Text), int.Parse(textBox1.Text));
            
            
        }
        void addup(int num1, int num2)
        {
            int answer;
            answer = num1 + num2;    
            MessageBox.Show("answer is = "+ answer.ToString());
            
        }
        private int subtract(int num1, int num2)
        {
            int answer;
            answer = num1 - num2;
           
            return answer;
        }
        void devide (int num1, int num2)
        {
            int answer;
            answer = num1 / num2;
            MessageBox.Show(answer.ToString());
        }
        void multply(int num1, int num2)
        {
            int answer;
            answer = num1 * num2;
            MessageBox.Show(answer.ToString());
        }

        private void buttonsubtract_Click(object sender, RoutedEventArgs e)
        {
            int num1;
            int num2;
            int returnvalue;
            num1 = int.Parse(textBox.Text);
            num2 = int.Parse(textBox1.Text);
            returnvalue = subtract(num1, num2);
            MessageBox.Show(returnvalue.ToString());
        }

        private void buttondivide_Click(object sender, RoutedEventArgs e)
        {
            int num1;
            int num2;
            num1 = int.Parse(textBox.Text);
            num2 = int.Parse(textBox1.Text);
            devide(num1, num2);

        }

        private void buttonmultiply_Click(object sender, RoutedEventArgs e)
        {
            int num1;
            int num2;
            num1 = int.Parse(textBox.Text);
            num2 = int.Parse(textBox1.Text);
            multply(num1, num2);
        }
    }
}
