# Activity-8

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace CALCARBSCALFAT
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private double fatCalories(double fatGrams)
        {
            return fatGrams * 9;
        }
       private double carbCalories(double carbGrams)
        {
            return carbGrams * 4;
        }


        private void label1_Click(object sender, EventArgs e)
        {

        }

        private void Form1_Load(object sender, EventArgs e)
        {
            
        }

        private void btnCalculate_Click(object sender, EventArgs e)
        {
            double calFromFat, fatGrams, calFromCarbs, carbGrams;

            if (double.TryParse(fatTextBox.Text, out fatGrams))
            {
                calFromFat = fatGrams * 9;

                calFatLabel.Text = calFromFat.ToString("nl");
            }
            else
            {
                MessageBox.Show("Enter Number For Fat In Grams!");
            }

            if (double.TryParse(carbsTextBox.Text, out carbGrams))
            {
                calFromCarbs = carbGrams * 4;

                calCarbsLabel.Text = calFromCarbs.ToString("nl");
            }

            else
            {
                MessageBox.Show("Enter Number For Carbs In Grams!");
            }
        }

        private void btnClear_Click(object sender, EventArgs e)
        {
            fatTextBox.Text = "";
            carbsTextBox.Text = "";
            calFatLabel.Text = "";
            calCarbsLabel.Text = "";
            fatTextBox.Focus();
        }

        private void btnClose_Click(object sender, EventArgs e)
        {
            this.Close();
        }

        private void carbsTextBox_TextChanged(object sender, EventArgs e)
        {
            
        }

        private void calFatLabel_Click(object sender, EventArgs e)
        {

        }
    }
}
