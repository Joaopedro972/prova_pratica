fn main() {
    let mut queue = Queue::new();

    queue.enqueue(1);
    println!("Elemento em fileira : 1");

    queue.enqueue(2);
    println!("Elemento em fileira: 2");

    if let Some(front) = queue.peek(){
        println!("Elemento na frente da fila: {}", front);

    }
    if let Some(dequeued) = queue.dequeued(){
        println!("Elemento desenfileirado: {}", dequeued);

    }
    println!("Fila atual: [");
    for (i, val) in queue.current_state().iter().enumerate(){
        if i !=0{
            print!(", ");

        }
        print!("{}", val);
    }
    println!("]");
    }

