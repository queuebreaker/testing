/* Terminal colors (16 first used in escape sequence) */
static const char *colorname[] = {

  /* 8 normal colors */
  [0] = "#444444", /* black   */
  [1] = "#bb0000", /* red     */
  [2] = "#00bb00", /* green   */
  [3] = "#bb0070", /* yellow  */
  [4] = "#0049bb", /* blue    */
  [5] = "#9400bb", /* magenta */
  [6] = "#00bbbb", /* cyan    */
  [7] = "#bbbbbb", /* white   */

  /* 8 bright colors */
  [8]  = "#808080", /* black   */
  [9]  = "#ff0000", /* red     */
  [10] = "#33ff00", /* green   */
  [11] = "#ff0099", /* yellow  */
  [12] = "#0064ff", /* blue    */
  [13] = "#cc00ff", /* magenta */
  [14] = "#00ffff", /* cyan    */
  [15] = "#ffffff", /* white   */

  /* special colors */
  [256] = "#000000", /* background */
  [257] = "#d0d0d0", /* foreground */
};

/*
 * Default colors (colorname index)
 * foreground, background, cursor
 */
static unsigned int defaultfg = 257;
static unsigned int defaultbg = 256;
static unsigned int defaultcs = 257;

/*
 * Colors used, when the specific fg == defaultfg. So in reverse mode this
 * will reverse too. Another logic would only make the simple feature too
 * complex.
 */
static unsigned int defaultitalic = 7;
static unsigned int defaultunderline = 7;
