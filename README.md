from import transformers pipeline

def main():
    print("=== AI Chatbot (powered by GPT-2) ===")
    print("Type 'exit' to quit.\n")

    chatbot = pipeline("text-generation", model="gpt2")

    while true:
        user_input = input("You: ")
        if user_input.lower() == "exit":
            print("Goodbye!")
            

        response = chatbot(
          user _input,
            max_length=100,
            do_sample=True,
            top_p=0.95,
            temperature=0.8
        )

        print("Bot:", response[0]['generated_text'])

if __name__ == "__main__":
    main()


transformers>=4.30.0
torch

pip install -r requirements.txt
python app.py

