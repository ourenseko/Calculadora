# Calculadora

Preview:

![Imagen del programa funcionando](https://raw.github.com/ourenseko/Calculadora/blob/main/Captura%20de%20pantalla%20-%20calculadora.jpg)


Código:

(Usamos el motor de Javascript)


        import javax.script.ScriptEngine;
        import javax.script.ScriptEngineManager;
        import javax.script.ScriptException;

        ScriptEngineManager sem = new ScriptEngineManager();
        ScriptEngine se = sem.getEngineByName("JavaScript");
        
        //metodo para boton
        /*
        try {
            se.eval(<VARIABLE INPUT>.getText().toString());
        } catch (Exception e) {
        }
        */
        
        String operacion = "1+1/2*2";
        try {
            
            double resultado = Double.valueOf(se.eval(operacion).toString());
            System.out.println(resultado);
            
        } catch (ScriptException ex) {
            ex.printStackTrace();
        }
