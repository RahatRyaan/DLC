# DLC Final Project
12
	switch (key)
    {
    case GLUT_KEY_RIGHT:
        if(dayornight == 0) {
            dayornight = 1;
        }else {
            dayornight = 0;
        }
        glutPostRedisplay();
        break;
    default:
        break;
    }
}
void credit(){

    cout<<"------------------------------------------------------"<<endl;
    cout<<"Computer Graphics- Final Project"<<endl;
    cout<<"\t 1. Faisal Amin Abir [20-43206-1]"<<endl;
    cout<<"\t 2. Neshat,Afrin Saidatun [21-44384-1]"<<endl;
    cout<<"\t 3. Taiyaba Akther [20-43189-1]"<<endl;
    cout<<"\t 4. Rahat Hasan Akanda [20-43133-1]"<<endl;

    cout<<"------------------------------------------------------"<<endl;

}



int main(int argc, char** argv){
    credit();
	glutInit(&argc, argv);
	glutInitDisplayMode(GLUT_SINGLE | GLUT_RGB);
	glutInitWindowPosition(0, 0);
	glutInitWindowSize(1900, 1900);
	glutCreateWindow("CG Project- Smart Village");
	init();
	glutDisplayFunc(display);
    glutSpecialFunc(keyboard);
    glutIdleFunc(windMill_start);
    //f = 0;
    // glutMouseFunc(handleMouse);
    glutTimerFunc(1000, update, 0);
    glutMainLoop();
}
