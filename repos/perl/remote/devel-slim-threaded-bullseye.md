## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:8fbffeae2b3d5f8a6308dd8aa6bc5a8b2352cce67ef84ca8fab98e63996f0e87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `perl:devel-slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:7ff1dfdfda36f9fa94606815e5f98d3542d4d71499cd4911742dbb0c371d1629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56756083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209e7f8bedfc200ebfcfbc181b7d88916f687f82c5c9b78daa4e483246a11219`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:46:18 GMT
WORKDIR /usr/src/perl
# Mon, 16 Mar 2026 23:01:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 16 Mar 2026 23:01:29 GMT
WORKDIR /usr/src/app
# Mon, 16 Mar 2026 23:01:29 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7344c79c6b9152f83f010c5f8c1def59036e8814b04f6e4b16581267a4f3ad45`  
		Last Modified: Mon, 16 Mar 2026 22:50:50 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4de18b8e85a46d7283457d77281382ca6be10f54123a2dea5b7f0ac1b1c4612`  
		Last Modified: Mon, 16 Mar 2026 23:01:40 GMT  
		Size: 26.5 MB (26497992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500bf0c9080eed66a6ce02591cdfc09bc7017c3b02c541584ddf71029fe921bc`  
		Last Modified: Mon, 16 Mar 2026 23:01:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:7d914b06aea5d3c94eecfefd0e133c9c459f66252a911b0229dc5c381925d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4147461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1605f7e3a69ca0cf057fc32bbfea8931a5b1cc864a1087d3be1a0421ab653c86`

```dockerfile
```

-	Layers:
	-	`sha256:4ed1bddd856bc40f851c90b67ec44c9713da50f664703c9c9d70a37beb67c69d`  
		Last Modified: Mon, 16 Mar 2026 23:01:40 GMT  
		Size: 4.1 MB (4129117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7342bd24ddb46dfc8101f467191e5426435e998f02c691f38141fda829993944`  
		Last Modified: Mon, 16 Mar 2026 23:01:39 GMT  
		Size: 18.3 KB (18344 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:464165192c6a116d69168636f4995b0a5141eaddfa30937cc7fc9cdea22bca1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49279766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef52315169f02b3fe137c5f79bf99c15b78b708ccd2cc3adab229b3eb1513fd`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:39:07 GMT
WORKDIR /usr/src/perl
# Tue, 17 Mar 2026 00:10:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 17 Mar 2026 00:10:48 GMT
WORKDIR /usr/src/app
# Tue, 17 Mar 2026 00:10:48 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:3bc17afcb32786a635d7faf13a7aa3a4142ac1a648b659c697f5e02460592774`  
		Last Modified: Mon, 16 Mar 2026 21:52:44 GMT  
		Size: 25.6 MB (25551392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce4528e551b15520a2d366ff956da8b5ef53437877a1848a4144de7fa0568a1`  
		Last Modified: Mon, 16 Mar 2026 23:44:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88599df15e5c171cb29013737d9dc54247f002fc8c66a0be6de9b44bd4f1ec75`  
		Last Modified: Tue, 17 Mar 2026 00:10:58 GMT  
		Size: 23.7 MB (23728108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0ef92f38532841cec473267821a0f68997995b009f30e1d9bf466255961d68`  
		Last Modified: Tue, 17 Mar 2026 00:10:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:1ceab118020cc805840caf144aa9c86bc8164b9cacdfc4805da868e06c0ceb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52188f9dbc30fdda561f56a7ea3d132c18053df50f94ee35241b31cd50db9c4d`

```dockerfile
```

-	Layers:
	-	`sha256:cb96c854f7aa48345f8bba3e440daf9c21e4b3ff0255a0482082c2b1554733d4`  
		Last Modified: Tue, 17 Mar 2026 00:10:58 GMT  
		Size: 4.1 MB (4103106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9a9c7fe36c5200d4c0f98dc5634d0f2dfe2b06fa037cebd4cf4cc82de08397b`  
		Last Modified: Tue, 17 Mar 2026 00:10:58 GMT  
		Size: 18.4 KB (18416 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c1c0cb9e6dfbbe3311f0830df9ac2547617c689236bd74987219d9aca680e48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54347981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057fb5f5d5c5a3bfd808e706be6ad3752db34ecbd07ccd38fae23ec53d5513ab`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:58:57 GMT
WORKDIR /usr/src/perl
# Mon, 16 Mar 2026 23:03:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 16 Mar 2026 23:03:52 GMT
WORKDIR /usr/src/app
# Mon, 16 Mar 2026 23:03:52 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65e68324b45e3324c484f6122e1229f1efb4da0efaf159a0ff4b8af8dd90b03`  
		Last Modified: Mon, 16 Mar 2026 23:04:03 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d562a3f341235548eca10c55dee69cfd629bcf1e941c5d3420f5ecc21fe965`  
		Last Modified: Mon, 16 Mar 2026 23:04:04 GMT  
		Size: 25.6 MB (25603190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf949774850e1f5885db0b4adc56a57bf190f79e82d63724edf0272f66eb240`  
		Last Modified: Mon, 16 Mar 2026 23:04:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:04e2770004743ee62f759a6319ba1ee319c962f9f5e5d1747bd155ca1088c9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cc41e325d09e01e13c35e1ad63570758e71d418a3c217d32b59a8c70d34cc4`

```dockerfile
```

-	Layers:
	-	`sha256:9290c095cf1fd6233ed1f80a522f7800be2c0353be98edd44cce92ece61ccd87`  
		Last Modified: Mon, 16 Mar 2026 23:04:04 GMT  
		Size: 4.1 MB (4103512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbcf63fe30886cd5eeba5afe8dc87bf7d6b85437a8995f112e47f345796aa103`  
		Last Modified: Mon, 16 Mar 2026 23:04:03 GMT  
		Size: 18.4 KB (18437 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:051d1e9f4c934b8d80d03144f1486f4788529fc9103159a17a95c3a7a69b7bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59249758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468f5f6e12edd8f769993a8b0bb59c546550dac83417fd122b0b2a543b145932`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:45:38 GMT
WORKDIR /usr/src/perl
# Mon, 16 Mar 2026 22:56:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 16 Mar 2026 22:56:53 GMT
WORKDIR /usr/src/app
# Mon, 16 Mar 2026 22:56:53 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:f9a1ac4759c4f531107bbcb94882648bc1b2c093ca00c3ddc1fe3d72957fb19a`  
		Last Modified: Mon, 16 Mar 2026 21:57:07 GMT  
		Size: 31.2 MB (31191663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ebfd313bbc07d4c39704cb64490c93d60b8dcc25f1b16aac960941433d6c64`  
		Last Modified: Mon, 16 Mar 2026 22:51:16 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3667f6566a448a86a9bcf8abf0a5a35f4f4952de4217f005f284e22c4577b7fc`  
		Last Modified: Mon, 16 Mar 2026 22:57:04 GMT  
		Size: 28.1 MB (28057830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a061ca8501e85f87a6cebf17402a559c8b3f7b957ea09b1c812c5951cf707709`  
		Last Modified: Mon, 16 Mar 2026 22:57:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:1b31f5220ed701a6b3912f73a5636df3ad6a4da7345db207687cd41080d8397a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04e22389f4765668467caae9f3fb201fd0c4100be2c4debfdce1cb7f1cfcf39`

```dockerfile
```

-	Layers:
	-	`sha256:562ce8d5b58897a7bbe47b1e07e8afc3fd09aa6aa5183bb0b6ac646dad66b4bf`  
		Last Modified: Mon, 16 Mar 2026 22:57:03 GMT  
		Size: 4.1 MB (4133399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1466c1eb3c74b24f6234e3f83037d067b45e85c8e8b805d89dfba30854c59736`  
		Last Modified: Mon, 16 Mar 2026 22:57:03 GMT  
		Size: 18.3 KB (18318 bytes)  
		MIME: application/vnd.in-toto+json
