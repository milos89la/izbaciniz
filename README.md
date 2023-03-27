# izbaciniz
izbaciniz

$matrica=[
    [2,4,7],
    [6,8,9],
    [3,4,5],
    [1,1,1],
    [8,67,4]
];
function print_matrix($m){
    for($i=0;$i<count($m) ;$i++){
        for($j=0;$j<count($m[$i]) ;$j++){
            echo $m[$i][$j]." ";
        }
        echo '<br>' ;

    }
}
print_matrix($matrica);
echo"<hr>";
function izbaci_najmanji_niz($m){
    $r= [];
    $n_index = 0;

    $t_najmanji=PHP_INT_MAX ;

    for($i=0;$i<count($m) ;$i++){
        $zbir=0;
        for($j=0;$j<count($m[$i]) ;$j++){
            $zbir+= $m[$i][$j];
            
        }
       if($zbir < $t_najmanji){
        $n_index = $i;
        $t_najmanji= $zbir;
       }

    }
    for($i=0;$i<count($m) ;$i++){
        if ($i!=$n_index){
            array_push($r,$m[$i]);
        }
    }
    return $r;

}
print_matrix(izbaci_najmanji_niz($matrica));
echo "<hr>";
