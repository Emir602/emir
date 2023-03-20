using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
using System.Collections;

namespace WindowsFormsApp8
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }
        List<object> Ülkeler = new List<object>();

        private void button1_Click(object sender, EventArgs e)
        {
            Ülkeler.Add(textBox1.Text);
        }

        private void button2_Click(object sender, EventArgs e)
        {
            int deger = Convert.ToInt32(textBox2.Text);
            label7.Text = Ülkeler[deger].ToString();
            

        }

        private void button3_Click(object sender, EventArgs e)
        {
            Ülkeler.Remove(textBox2.Text);
        }

        private void button4_Click(object sender, EventArgs e)
        {
           Ülkeler.Clear();
        }

        private void button8_Click(object sender, EventArgs e)
        {
            Ülkeler.Insert(Convert.ToInt32(textBox2),textBox1.Text);
        }

        private void button5_Click(object sender, EventArgs e)
        {

            for (int a = 0; a < Ülkeler.Count; a++)
            {
                listBox1.Items.Add(Ülkeler[a]);
            }
        }

        private void button10_Click(object sender, EventArgs e)
        {
            if (Ülkeler.Contains(textBox5.Text))
            {
                label6.Text = "bulundu";
                label6.ForeColor = Color.Green;
            }
            else
            {

                label6.Text = "bulunmadı";
                label6.ForeColor = Color.Red;
            }
        }

        private void button6_Click(object sender, EventArgs e)
        {
            listBox1.Items.Clear();
        }

        private void button9_Click(object sender, EventArgs e)
        {
            int artmak = listBox1.SelectedIndex;
            Ülkeler.Insert(artmak + 1, textBox1.Text);
        }

        private void button7_Click(object sender, EventArgs e)
        {
            Ülkeler.Remove(listBox1.SelectedItem);
        }
    }
}
