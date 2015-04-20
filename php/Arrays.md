PHP arrays snippets
===================

    /**
     * Just like array_filter operates on keys instead.
     * 
     * @param  array    $arr      Array
     * @param  callable $callback The callback function to use. Should return TRUE for items in array that should be preserved.
     * 
     * @return array              Filtered array
     */
    function array_filter_keys($arr, $callback) {
        return array_intersect_ukey($arr, $arr, function($k1, $k2) use ($callback) {
            return call_user_func($callback, $k1) ? 0 : 1;
        });
    }

    