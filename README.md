# ProjetoFormsMultiplo
CRIE UM PROJETO DE FORMA QUE A PESSOA INFORME UM VALOR INTEIRO E AO CLICAR EM UMA LABEL EXIBA SE O VALOR INFORMADO É OU NÃO MÚLTIPLO DE 7.

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace ProjetoFormsMultiplo
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

private void btnVerificar_Click(object sender, EventArgs e)
        {
            if (string.IsNullOrEmpty(txtNumero.Text))
            {
                lblResultado.Text = "Por favor, insira um número.";
                return;
            }
            if (int.TryParse(txtNumero.Text, out int numero))
            {
                if (numero % 7 == 0)
                {
                    lblResultado.Text = $"{numero} é múltiplo de 7.";
                }
            }
            else
            {
                lblResultado.Text = "Entrada inválida. Por favor, insira um número inteiro.";
            }

  }
}
}
