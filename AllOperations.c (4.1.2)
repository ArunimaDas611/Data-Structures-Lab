struct Node
{
	int data;
	struct Node* next;
};
typedef struct Node* NODE;
NODE createNode(int data)
{
	NODE new = (struct
	            Node*)malloc(sizeof(struct Node));
	if(new == NULL)
	{
		printf("Memory allocation failed\n");
		exit(1);
	}
	new -> data = data;
	new -> next = NULL;
	return new;
}
NODE addNode(NODE list, int data)
{
	NODE temp = createNode(data);
	if(list == NULL)
	{
		list = temp;
	}
	else
	{
		NODE last = list;
		while(last -> next != NULL)
		{
			last = last -> next;
		}
		last -> next = temp;
	}
	return list;
}
void displayList(NODE list)
{
	NODE temp = list;
	while(temp != NULL)
	{
		printf("%d --> ", temp -> data);
		temp = temp -> next;
	}
	printf("NULL\n");
}
NODE concatenate(NODE l1, NODE l2)
{
	if(l1 == NULL)
	{
		return l2;
	}
	NODE temp = l1;
	while(temp -> next != NULL)
	{
		temp = temp -> next;
	}
	temp -> next = l2;
	return l1;
}
