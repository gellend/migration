# Zsh and Oh My Zsh Installation

1.  **Check your current shell:**

    ```bash
    echo $SHELL
    ```

2.  **Install Zsh:**

    ```bash
    sudo dnf install zsh
    ```

3.  **Install Oh My Zsh:**

    I recommend visiting the official webpage [ohmyz.sh](https://ohmyz.sh/) for installation instructions.

4.  **Install Plugins:**

    a. **zsh-syntax-highlighting:**

        ```bash
        git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
        ```

    b. **zsh-autosuggestions:**

        ```bash
        git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
        ```

5.  **Configure .zshrc:**

    Edit the `plugins` section inside the `.zshrc` file:

    ```bash
    plugins=(
        git
        zsh-autosuggestions
        zsh-syntax-highlighting
    )
    ```

6.  **Apply all changes**

    ```bash
    omz reload

    ```

7.  **Log out**

    Don't forget to log out so that the changes takes effect

8.  **Checkout the official Cheatsheet**

    [Cheatsheet](https://github.com/ohmyzsh/ohmyzsh/wiki/Cheatsheet)
