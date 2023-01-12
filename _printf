int _printf(const char *format, ...)
{
    int chars_printed = 0;
    va_list args;

    va_start(args, format);
    while (*format)
    {
        if (*format == '%')
        {
            format++;
            switch (*format)
            {
                case 'c':
                    putchar(va_arg(args, int));
                    chars_printed++;
                    break;
                case 's':
                    chars_printed += printf("%s", va_arg(args, char *));
                    break;
                case '%':
                    putchar('%');
                    chars_printed++;
                    break;
                default:
                    break;
            }
        }
        else
        {
            putchar(*format);
            chars_printed++;
        }
        format++;
    }
    va_end(args);

    return chars_printed;
}
