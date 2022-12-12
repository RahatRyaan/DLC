# DLC Final Project
12
int main(int argc, char** argv){
    credit();
	glutInit(&argc, argv);
	glutInitDisplayMode(GLUT_SINGLE | GLUT_RGB);
	glutInitWindowPosition(0, 0);
	glutInitWindowSize(1900, 1900);
	glutCreateWindow("CG Project- Smart Village");
	init();
	glutDisplayFunc(display);
    glutKeyboardFunc(handleKeypress);
    glutMouseFunc(handleMouse);
    glutTimerFunc(1000, update, 0);
    glutMainLoop();
}
