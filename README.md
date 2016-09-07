
# NAME

Test::Deep::ArrayEachNotEmpty - an alternative to Test::Deep::ArrayEach

# SYNOPSIS

    use Test::Deep;
    use Test::Deep::ArrayEachNotEmpty;

    my $empty = [];
    my $array = [{ foo => 1 }];

    cmp_deeply $empty, array_each({ foo => 1 });
    # => pass

    cmp_deeply $array, array_each({ foo => 1 });
    # => pass

    cmp_deeply $empty, array_each_not_empty({ foo => 1 });
    # => fail

    cmp_deeply $array, array_each_not_empty({ foo => 1 });
    # => pass

# DESCRIPTION

Test::Deep::ArrayEachNotEmpty is a sub class of Test::Deep::ArrayEach
which forbid an empty array.

# LICENSE

Copyright (C) Mihyaeru.

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# AUTHOR

Mihyaeru <mihyaeru21@gmail.com>
