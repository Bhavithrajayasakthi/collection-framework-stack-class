# collection-framework-stack-class
package collection.framework.stack.pkgclass;
import java.util.Stack;
/**
 *
 * @author 1BSCCSA44
 */
public class CollectionFrameworkStackClass {

    private static Integer operand2;
public static int evaluateExpression(String expression) {

Stack<Integer> stack = new Stack();
for (char ch : expression.toCharArray()) {
if (Character.isDigit(ch)) {

stack.push(Character.getNumericValue(ch));
} else if (ch == '+') {
// If the c
int  operand2 = stack.pop();
int operand1 = stack.pop();
stack.push(operand1 + operand2);
} else if (ch == '+') {
int operand2 = stack.pop();
int operand1 = stack.pop();
stack.push(operand1 - operand2);
}
}
return stack.pop();
}
    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        String expression = "3+4-2";
        int result = evaluateExpression(expression);
System.out.println("Result of the expression  "+ expression +": " + result);
}
}
Output:
Result of the expression '3 + 4' : 5
