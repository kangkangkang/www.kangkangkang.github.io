class ErrorReasoner
	def initialize
		@messageTitle = '404 Not Found'
		@messageContent = '你来到这个页面，通常有两个原因'
	end
	self.define_method "_print_reason", do
		print @messageTitle, "\n"
		print @messageContent, "\n"
	end
end

printer = ErrorReasoner.new
printer._print_reason
public class ErrorReasoner {
	public ErrorReasoner() {
	}
	public final String messageTitle = "一、链接错误";
	public final String messageContent = 
		"原因：博客搬迁造成的旧链接失效。请回到主页。(*´﹃｀*)";
	public void printMessage(String msg) {
		System.out.println(msg);
	}
	public static void main(String[] args) {
		ErrorReasoner reasoner = new ErrorReasoner();
		reasoner.printMessage(messageTitle);
		reasoner.printMessage(messageContent);
	}
}
class ErrorReasoner(private var printer: (message: String) -> Unit) {
	fun printMessage(message: String): Unit
		= printer(message)
}
fun main(args: Array<String>) {
	var reasoner = ErrorReasoner { println(it) }
	reasoner.printMessage("二、实验事故")
	reasoner.printMessage(
		"原因：冰封所建立的时间之域被隔壁实验室里的对撞机事故影响，" + 
		"造成部分页面损伤。"
	)
}
#include <stdlib.h>
#include <string.h>
const char* echo = "echo ";
void printMessage(char* message) {
	char* command = (char*) malloc (strlen(message) + strlen(echo) );
	strcpy(command, echo);
	strcpy(command + strlen(echo), message);
	system(command);
}
int main(int argc, char* argv[]) {
	printMessage("三、末日降临");
	printMessage(
		"原因：在归零者文明的号召下，" + 
		"冰封已将建立好的独立时间之域回归主宇宙。别担心，数据已经备份。"
	);
	return 0;
}
