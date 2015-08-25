FROM nate/basedev

RUN apt-get update && apt-get install perl-doc perltidy groff build-essential -y
RUN curl -L https://cpanmin.us | perl - App::cpanminus

RUN cpanm Test::Trap
RUN cpanm File::Slurp
RUN cpanm Minilla

