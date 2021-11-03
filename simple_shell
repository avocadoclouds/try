#include "shell.h"

char *lsh_read_line(void);
char **lsh_split_line(char *line);
int lsh_launch(char **args);
int lsh_execute(char **args);
int lsh_num_builtins();
int lsh_cd(char **args);
int lsh_help(char **args);
int lsh_exit(char **args);



void lsh_loop(void)
{
  char *line;
  char **args;
  int status;

  do {
    printf("Shark$ ");
    line = lsh_read_line();
    args = lsh_split_line(line);
    status = lsh_execute(args);

    free(line);
    free(args);
  } while (status);
}

int main(int argc, char **argv)
{


  lsh_loop();



  return EXIT_SUCCESS;
}

