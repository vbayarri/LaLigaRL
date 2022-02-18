El objetivo del proyecto es realizar una prueba de aprendizaje con reinforcement learning sobre apuestas deportivas.

- Agente (apostador): 
    - En cada turno decide las apuestas a realizar.
- Environment (casa de apuestas):
    - Cada sesión de LaLiga será una partida distinta.
    - La partida termina si:
        - El jugador se queda sin fondos.
        - Se acaban todas las jornadas de la competición.
    - El importe de la apuesta y el presupuesto disponible serán variables iniciales del programa.
- Observaciones (jornada de liga):
    - Las observaciones serán los partidos de la jornada con los datos estadísticos de cada equipo (reutilizar preproceso del proyecto anterior)
- Acciones disponibles ();
    - 10 partidos por jornada para apostar
    - Se simplifica el proceso de decisión. ¿En cada partido decide si apostar o no. No se indica la cantidad? Ver ejemplo del coche.

- ¿Qué espero obtener?
    - Conocimiento de los algoritmos
    - Un algorimo para invertir dinero en las casas de apuestas

Proceso de ataque del proyecto:
    - Nicholas Renotte
        - Reinforcement Learning in 3 Hours | Full Course using Python => Curso entero viendo como se monitoriza el aprendizaje.
        - Building a Custom Environment for Deep Reinforcement Learning with OpenAI Gym and Python => Crear un env
        
        - Build a Doom AI Model with Python | Gaming Reinforcement Learning Full Course => Centrado en crear un propio environment
        - AI learns to DESTROY Street Fighter => Centrado en hyperparameter opt
    - Ver el video de Nicholas Renotte de RL sobre aprendizaje con el coche.
    - Video de Nicholas Renotte de RL sobre inversión:
        - Stable_baselines y un entorno específico para GYM.
        - Utiliza el algoritmo A2C que implementa por debajo un LTSM.
        - Transforma los datos a una tendencia de variación
        - Utiliza una ventana de aprendizaje de x posiciones.
        - Pasar a una nota de aprendizaje.
        - Se requiere Tensorflow. Revisar si ya se puede usar la versión de TensorFlow diseñada para equipos con M1.
            - Las instrucciones para instalar Tensorflow con el soporte de GPU están en:
                https://developer.apple.com/metal/tensorflow-plugin/
            - Está previsto para las versiones de TF 2.5 y 2.6 con Python 3.8 y 3.9
            - El paquete stable_baselines está fuera de soporte:
                Stable-Baselines supports Tensorflow versions from 1.8.0 to 1.15.0, and does not work on Tensorflow versions 2.0.0 and above. PyTorch support is done in Stable-Baselines3
            - Utilizar el paquete de stable_baselines_3:
                https://stable-baselines3.readthedocs.io/en/master/
                Stable-Baselines3 requires python 3.7+ and PyTorch >= 1.8.1.
                No utiliza TF.
    - Revisar el planteamiento:
        - RL sólo
        - RL with CNN
        - RL with two Models
    - Crear un entorno virtual con las librerías


Ideas:
    - Documentación:
        - ¿Cómo documento el proceso de aprendizaje?
        - Notas en un readme.
        - Una sección en Notion
        - Un video en Youtube.
    - Granularidad:
        - ¿Es mejor entrenar un bot para la liga de cada país o un bot sobre el comportamiento del futbol en general?
        - ¿Es mejor crear un bot para toda la competición o crear un bot independiente para la evolución de cada equipo?
        - ¿Combinarlos?
    - Entrenamiento:
        - ¿Qué efeto tiene en la predicción las features precalculadas?
            - Racha de victorias y pártidos perdidos
    - Algoritmo:
        - En el video del trading se utiliza una LSTM
        - ¿Hay opción para utilizar transformers? Simpr
        - ¿Cuál es el nuevo trend en IA que substituye a los transformers?
    - Combinación:
        - ¿Es mejor juntar la probabilidad de victoria con la estrategia inversora o separarlo?
