// binSort_linearList_Chain
template <typename T>
void Chain<T>::binSort(int range) {
    chainNode<T> **bottom, **top;
    bottom = new chainNode<T> *[range + 1](nullptr);
    top = new chainNode<T> *[range + 1](nullptr);
    for (; header != nullptr; header = header->next) {
        int index = header->element;
        if (bottom[index] == nullptr)
            bottom[index] = header;
        else {
            top[index]->next = header;
            top[index] = header;
        }
    }
    chainNode<T> *tmp = nullptr;
    for (int index = 0; index <= range; index++) {
        if (bottom[index] == nullptr)
            continue;
        if (tmp == nullptr)
            header = bottom[index];
        else
            tmp->next = bottom[index];
        tmp = top[index];
    }
    if (tmp != nullptr)
        tmp->next = nullptr;
    delete[] bottom;
    delete[] top;
}
