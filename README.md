public static void kiirToFile(Collection<Flotta> flottas) throws IOException {
        int i = 1;
        for(var flotta : flottas){
            File myObj = new File("lista"+i+".txt");
            flotta.kiir("lista"+i+".txt");
            i++;
        }
    }

    public static void novel(Collection<Legitarsasag> legitarsasags,int db){

        for (Iterator<Legitarsasag> iterator = legitarsasags.iterator(); iterator.hasNext();) {
            Legitarsasag legitarsasag = iterator.next();
            for(int i = 0 ; i < legitarsasag.repulogepList.size();i++){

                if(legitarsasag.repulogepList.get(i).getClass() == Utasszallito.class &&
                        legitarsasag.repulogepList.get(i).getGyarto().equalsIgnoreCase("Airbus")){
                    ((Utasszallito) legitarsasag.repulogepList.get(i)).setFerohely(((Utasszallito) legitarsasag.repulogepList.get(i)).getFerohely()+db);
                }

            }
        }



https://arato.inf.unideb.hu/panovics.janos/beugrok_Java.pdf
