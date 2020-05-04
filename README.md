import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    Scanner leitor = new Scanner(System.in);
      
    System.out.println("Escolha o modelo: cubo, cilindro, cone, esfera.");
    String figura = leitor.nextLine();//FIGURA
    if (figura.equals("cubo")){
      System.out.println("area ou volume?");
      String formula = leitor.nextLine();
      if (formula.equals("area")){
        System.out.println("qual é o valor da aresta?");
        float a = leitor.nextInt();
        double potencia = Math.pow(a, 2);
        double area_cubo = 6 * potencia;
        System.out.println("Área do cubo: " + area_cubo);
      }else{//CALCULAR VOLUME DO CUBO
      System.out.println("qual é o valor da aresta?");
      float a = leitor.nextInt();
      double potencia = Math.pow(a, 3);
      double volume_cubo = potencia;
      System.out.println("Volume do cubo: " + volume_cubo);
      }

    }else if (figura.equals("cilindro")){//CALCULAR O CILINDRO
      System.out.println("area ou volume?");
      String formula = leitor.nextLine();
      if (formula.equals("area")){//CALCULAR A ÁREA DO CILINDRO
        System.out.println("Qual é o valor do raio da base?");
        float r = leitor.nextInt();
        System.out.println("Qual é o valor da altura do cilindro?");
        float h = leitor.nextInt();
        double area_lado = (2 * (Math.PI) * r * h);
        double area_base = ((Math.PI) * r * r);
        double area_cilindro = (area_lado + area_base);
        System.out.println("A área do cilindro é: " + area_cilindro);
      }else{//CALCULAR O VOLUME DO CILINDRO
        System.out.println("Qual é o valor do raio da base?");
        float r = leitor.nextInt();
        System.out.println("qual é a altura do cilindro?");
        float h = leitor.nextInt();
        double area_base = ((Math.PI) * r * r);
        double volume_cilindro = (area_base * h);
        System.out.println("Volume do cilindro: " + volume_cilindro);
      }

    }else if (figura.equals("esfera")){//ESCOLHEU A ESFERA
      System.out.println("area ou volume?");
      String formula = leitor.nextLine();
      if(formula.equals("area")){//ESCOLHEU A ÁREA
        System.out.println("qual é o valor do raio?");
        float r = leitor.nextInt();
        double area_esfera = (4 * (Math.PI) * r * r);
        System.out.println("Área da esfera: " + area_esfera);
        
      }else{//ESCOLHEU O VOLUME
        System.out.println("Qual é o valor do raio?");
        float r = leitor.nextInt();
        double volume_esfera = (4/3 * (Math.PI) * r * r * r);
        System.out.println("Volume da esfera: " + volume_esfera);
      }

    }else if(figura.equals("cone")){
      System.out.println("area ou volume?");
      String formula = leitor.nextLine();
      if (formula.equals("area")){
        System.out.println("Qual é o valor do raio?");
        float r = leitor.nextInt();
        System.out.println("Qual é a altura do cone?");
        float h = leitor.nextInt();
        double g_pow = ((r * r)+(h * h));
        double g = Math.sqrt(g_pow);
        double area_cone = ((Math.PI) * r * (g + r));
        System.out.println("Área do cone: " + area_cone);        
      }else{
        System.out.println("Qual é o valor do raio?");
        float r = leitor.nextInt();
        System.out.println("Qual é o valor da altura do cone?");
        float h = leitor.nextInt();
        double volume_cone = ((Math.PI) * r * r * h)/3;
        System.out.println("Volume do cone: " + volume_cone);
      }
    }
  }
}
