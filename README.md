# temizlik_robotu

TEMIZLIK ROBOTU Metapackage

Workspace yok ise workspace oluşturunuz.

Örn. http://wiki.ros.org/catkin/Tutorials/create_a_workspace

    cd
    mkdir -p workspace/src

Daha sonra workspace gidiniz ve paketi indiriniz. interactive_marker_twist_server paketi de gerekiyor.

    cd workspace/src
    git clone "https://github.com/inomuh/temizlik_robotu.git"
    git clone https://github.com/ros-visualization/interactive_marker_twist_server.git
    rosdep install --from-paths ~/workspace/src --ignore-src
    gedit ~/.bashrc
    export GAZEBO_MODEL_PATH=~/workspace/src/temizlik_robotu/:$GAZEBO_MODEL_PATH
    cd ..
    catkin_make
    catkin_make install
    source devel/setup.bash
    roslaunch temizlik_robotu_baslat temizlik_robotu_baslat.launch

Görev tamamlama yüzdesini görmek için

    roslaunch temizlik_robotu_bilgi_servisi temizlik_robotu_bilgi_servisi_baslat.launch
