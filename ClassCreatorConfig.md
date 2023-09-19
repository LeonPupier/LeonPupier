# VSCode C++ Class Creator plugin configuration

### Header file
```c++
/* ************************************************************************** */
/*                                                                            */
/*                                                        :::      ::::::::   */
/*   Serialization.hpp                                  :+:      :+:    :+:   */
/*                                                    +:+ +:+         +:+     */
/*   By: lpupier <lpupier@student.42lyon.fr>        +#+  +:+       +#+        */
/*                                                +#+#+#+#+#+   +#+           */
/*   Created: 2023/07/17 08:27:16 by lpupier           #+#    #+#             */
/*   Updated: 2023/09/19 10:26:14 by lpupier          ###   ########.fr       */
/*                                                                            */
/* ************************************************************************** */

#ifndef {{*CLASSNAMEUPPER*}}_HPP
# define {{*CLASSNAMEUPPER*}}_HPP

# include <iostream>

# define RESET		"\033[0m"
# define BLACK		"\033[30m"
# define RED		"\033[31m"
# define GREEN		"\033[32m"
# define YELLOW		"\033[33m"
# define BLUE		"\033[34m"
# define MAGENTA	"\033[35m"
# define CYAN		"\033[36m"
# define WHITE		"\033[37m"

class {{*CLASSNAME*}} {

public:

	// Init
	{{*CLASSNAME*}}();
	{{*CLASSNAME*}}(const {{*CLASSNAME*}} &obj);
	~{{*CLASSNAME*}}(void);
	{{*CLASSNAME*}} &operator=(const {{*CLASSNAME*}} &obj);

	// Body

};

#endif
```

### Code file
```c++
/* ************************************************************************** */
/*                                                                            */
/*                                                        :::      ::::::::   */
/*   Serialization.cpp                                  :+:      :+:    :+:   */
/*                                                    +:+ +:+         +:+     */
/*   By: lpupier <lpupier@student.42lyon.fr>        +#+  +:+       +#+        */
/*                                                +#+#+#+#+#+   +#+           */
/*   Created: 2023/07/17 08:27:14 by lpupier           #+#    #+#             */
/*   Updated: 2023/09/19 10:35:49 by lpupier          ###   ########.fr       */
/*                                                                            */
/* ************************************************************************** */

#include "{{*HEADERFILENAME*}}"

// Init
{{*CLASSNAME*}}::{{*CLASSNAME*}}()
{
	std::cout << GREEN << "[LOG] " << RESET << "{{*CLASSNAME*}} class has been created" << std::endl;
}

{{*CLASSNAME*}}::{{*CLASSNAME*}}(const {{*CLASSNAME*}} &obj)
{
	*this = obj;
}

{{*CLASSNAME*}}::~{{*CLASSNAME*}}(void)
{
	std::cout << RED << "[LOG] " << RESET << "{{*CLASSNAME*}} class has been destroyed" << std::endl;
}

{{*CLASSNAME*}} &{{*CLASSNAME*}}::operator=(const {{*CLASSNAME*}} &obj)
{
	(void)obj;
	return (*this);
}

// Body
```

Bisous 🦩
