# Kalkylator2
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Kalkylator
{
    public partial class Form1 : Form
    {
        double value = 0;
        string operation = "";
        bool operation_pressed = false;

        public Form1()
        {
            InitializeComponent();
        }

        private void button_Click(object sender, EventArgs e)
        {
            Button b = (Button)sender;
            result.Text = result.Text + b.Text;
            if ((result.Text == "0") || (operation_pressed)) 
                result.Clear();
            operation_pressed = false;
            
        }

        private void btnoperator_Click(object sender, EventArgs e)
        {
            Button b = (Button)sender;
            operation = b.Text;
            value = double.Parse(result.Text);
            operation_pressed = true;
            equation.Text = value + " " + operation;
            if ((result.Text == "0") || (operation_pressed = true))
                result.Clear();


        }

        private void btnsvar_Click(object sender, EventArgs e)
        {
            equation.Text = "";
            switch (operation)
            {
                case "+":
                    result.Text = (value + double.Parse(result.Text)).ToString();
                    break;
                case "-":
                    result.Text = (value - double.Parse(result.Text)).ToString();
                    break;
                case "*":
                    result.Text = (value * double.Parse(result.Text)).ToString();
                    break;
                case "/":
                    result.Text = (value / double.Parse(result.Text)).ToString();
                    break;
                default: 
                    break;

            }//end swtich
            operation_pressed = false;
        }

        private void btn_Click(object sender, EventArgs e)
        {
            
        }

        private void btn0_Click(object sender, EventArgs e)
        {
            Button b = (Button)sender;
            result.Text = result.Text + b.Text;
        }
        
        private void btn1_Click(object sender, EventArgs e)
        {

            Button b = (Button)sender;
            result.Text = result.Text + b.Text;
        }

        private void btn2_Click(object sender, EventArgs e)
        {

            Button b = (Button)sender;
            result.Text = result.Text + b.Text;
        }

        private void btn3_Click(object sender, EventArgs e)
        {

            Button b = (Button)sender;
            result.Text = result.Text + b.Text;
        }

        private void btn4_Click(object sender, EventArgs e)
        {

            Button b = (Button)sender;
            result.Text = result.Text + b.Text;
        }

        private void btn5_Click(object sender, EventArgs e)
        {

            Button b = (Button)sender;
            result.Text = result.Text + b.Text;
        }

        private void btn6_Click(object sender, EventArgs e)
        {

            Button b = (Button)sender;
            result.Text = result.Text + b.Text;
        }
        
        private void btn7_Click(object sender, EventArgs e)
        {

            Button b = (Button)sender;
            result.Text = result.Text + b.Text;
        }

        private void btn8_Click(object sender, EventArgs e)
        {

            Button b = (Button)sender;
            result.Text = result.Text + b.Text;
        }

        private void btn9_Click(object sender, EventArgs e)
        {

            Button b = (Button)sender;
            result.Text = result.Text + b.Text;
        }

        private void btnkomma_Click(object sender, EventArgs e)
        {
            Button b = (Button)sender;
            result.Text = result.Text + b.Text;
        }

        private void btnC_Click(object sender, EventArgs e)
        {
            if ((result.Text == "0") || (operation_pressed))
                result.Clear();

        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }

        private void btnce_Click(object sender, EventArgs e)
        {
            result.Clear();
            value = 0;
        }

        private void label1_Click(object sender, EventArgs e)
        {

        }

        private void result_TextChanged(object sender, EventArgs e)
        {
            
        }
    }
}
