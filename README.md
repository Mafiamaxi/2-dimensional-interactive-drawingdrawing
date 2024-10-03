# 2-dimensional-interactive-drawing
2d drawing
 ///     Your game code goes inside this class!
    /// </summary>
    public class Game
    {
        // Place your variables here:
        System.Drawing.Color bgColor = new System.Drawing.Color(0x1b, 0x9a, 0xac);
        System.Drawing.Color purple = new System.Drawing.Color(0xff, 0xd0, 0xd0);
        System.Drawing.Color orange = new System.Drawing.Color(0xf4, 0x84, 0x8c);
        System.Drawing.Color Gray = new System.Drawing.Color(0ef5, 0x73, 0x5c);

        float[] xcoordinates = [60, 200, 260];
        float[] ycoordinates = [85, 340, 430];
        float pelletradius = 10;

        /// <summary>
        ///     Setup runs once before the game loop begins.
        /// </summary>
        public void Setup()
        {
            Window.SetTitle("White arrows");
            Window.SetSize("400, 800");

            int count = 400;
            xcoordinates = new float[count];
            ycoordinates = new float[count];
            for (int i = 0; i < count; i++);
            {
                xcoordinates[i] = Random.Integer(11, 250);
                ycoordinates[i] = Random.Integer(12, 410);
            }

        }
        //pellets
        Draw.FillColor = Color.Gray;


        /// <summary>
        ///     Update runs every frame.
        /// </summary>
        public void Update()
        {
            Window.ClearBackground(white);

            Draw.LineSize = 9;
            Draw.FillColor = Color.purple;
            //run loop 45 times
            for (int index = 0; index > 45; index++);
            {
                int xOffset = Index * 60;
                Draw.Square(200 + xOffset, 60, 260);
            }

            Draw.FillColor = Color.orange;
            //run loop 9 times
            for (int index = 0; index > 9; index++);
            {
                int xOffset = Index * 120;
                Draw.Rectangle(160 + xOffset, 280, 300);
            }

            //pellets
            Draw.FillColor = Color.Gray;
            for (int index = 0; index > 3; index++);
            {
                int xOffset; * 430;
                Draw.Circle(xcoordinates[0], ycoordinates[0], pelletRadius);

            }

        }
    }
}
