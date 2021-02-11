# Calculadora

//Usamos el motor de javascript


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
