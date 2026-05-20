## `perl:5-slim-threaded`

```console
$ docker pull perl@sha256:e4befa2d52eda1bf5669468a226abe021c510edbbe9d4927239eeea7bd31c209
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `perl:5-slim-threaded` - linux; amd64

```console
$ docker pull perl@sha256:b232ee5d7bffd8c728c3c50a67d69d53a9234a58b29839123db29a605d615220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61791214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94427acb6ee5f50a78a0416c66e925c1fad552a777a707e8574074411a786ef`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:28:59 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:34:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:34:06 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:34:06 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d1153460951126d8992b280f0be82497a1bf4261fb47e877b52b05b207bf37`  
		Last Modified: Tue, 19 May 2026 23:34:12 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6417c619229b2c44e4481e4c2747bcde3d8556cd26a4eb6bf8d6979bd53d7d`  
		Last Modified: Tue, 19 May 2026 23:34:19 GMT  
		Size: 32.0 MB (32011020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17024f1b001346b236d7d5564dcfd59dafd069dd945652f20445ebabca35e88`  
		Last Modified: Tue, 19 May 2026 23:34:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:feb8a67e71118c20f37736a34593f77d92b11bb3abf3b84bfcd4e72baf090932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4943dd73245097fc916f64f85d1d89a7c25b81c05ccdc2f25e7620edf454f17a`

```dockerfile
```

-	Layers:
	-	`sha256:695f0edd23047f309066eca16c1096deb5a2baecb8a542b504cad82f59c71552`  
		Last Modified: Tue, 19 May 2026 23:34:18 GMT  
		Size: 4.0 MB (4010908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:382ff4cbf76ab3b5beba6df767d867049d55adc3d4862c52040d95a5cf065871`  
		Last Modified: Tue, 19 May 2026 23:34:17 GMT  
		Size: 20.5 KB (20483 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:51bfdc916b6f8637aec3818686758b06868bf2808666ac99044e0506fabbd7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57166999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc385919ddb506a93b2942900b05d3feb69ffa649db12d61db5772b016ce7644`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:58:11 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 21:04:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 21:04:09 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 21:04:09 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0867b237d0e94f40d9cecbd78a737a317f74a830a9de0c38d8c44b00d3ecb31`  
		Last Modified: Fri, 08 May 2026 21:04:19 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630729944a00f48ded39bd419f18c8a3e737fde71c9d3784b3c84b24462a0bd3`  
		Last Modified: Fri, 08 May 2026 21:04:20 GMT  
		Size: 29.2 MB (29218530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c32f1adbbd9eabed3bb4bef50a0f37cf29ccab7c14b4fddd6c048f7782c9f1a`  
		Last Modified: Fri, 08 May 2026 21:04:19 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:5f9ab89fcac2a36ce23e89de1a3f5414d5abc4471ecc2f136f32f0dccc9498fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1562ad825d99fd0d5f11fd216bbab31d102fccf50cf40faa63555433fc13640`

```dockerfile
```

-	Layers:
	-	`sha256:8e773308c44f16486bc5e61c59c1f69b62301ed44b2108743dbb34edc8e1714d`  
		Last Modified: Fri, 08 May 2026 21:04:19 GMT  
		Size: 4.0 MB (4003907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b697c6707efd87a8bd98a7355eadc90f613903b664a4dad8fb5a2c8f3201ba`  
		Last Modified: Fri, 08 May 2026 21:04:19 GMT  
		Size: 20.6 KB (20610 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:138269239c36ddc9d7767898ff3e9922823ebffad2c2c55f9804fd1b89689442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54501967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0976dd184e5464a92dd7e06688be40a262dedb69cb7ad1275deaf5bf9e8cebe7`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:47:35 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 19:53:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 19:53:22 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 19:53:22 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1210c36699dcca0e64f2441a755de4342b7adb1099b97082531a86e5456793`  
		Last Modified: Fri, 08 May 2026 19:53:33 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b84cffd2fb63bd0f0eafc0ed6ef9d3c4ec3164b978f1b725cc93c56f1b8024`  
		Last Modified: Fri, 08 May 2026 19:53:34 GMT  
		Size: 28.3 MB (28286786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07833a7a0167ccb3a099808039b517402f7ff91988996fa14a55cc32445d599d`  
		Last Modified: Fri, 08 May 2026 19:53:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:6d028cdae1bae4bbfd72d8837d7969f7f953d820ade32067cfde6d6797cc26dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5215c44a4e26bc86bdb64e406b5e7680266e8fc4b412527d2627c97f817318`

```dockerfile
```

-	Layers:
	-	`sha256:e24d07b7e8adad64ad99394aa5225d55bc5333077d017a5bf9f269450ffc03b0`  
		Last Modified: Fri, 08 May 2026 19:53:33 GMT  
		Size: 4.0 MB (4003098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:397cf28ce24053674ca364a3c145c3f07e8a272391c46d9374f8472c8d7c489e`  
		Last Modified: Fri, 08 May 2026 19:53:32 GMT  
		Size: 20.6 KB (20611 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:da0274c1d165e26013cd604348a1da26ebf35c8df38c825f0b8d768b139c9627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61815361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c9caee38e269cedee3c5497014c99ed67f1c660e5485237a039b8e7d63dae6`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:32:20 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:37:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:37:40 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:37:40 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ac59f62174f98abce878fa5b055bb9e7707b6672833a7682adad2574c9b57`  
		Last Modified: Tue, 19 May 2026 23:37:51 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35eb635b17b646cd8dfe355666dcbbbc82fdfdd48f1f11fadcf44bb1019a75a`  
		Last Modified: Tue, 19 May 2026 23:37:52 GMT  
		Size: 31.7 MB (31673174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710f4aab162d3b0e7d511076021990b7e5ba5330e3c6d6cb9f418aec57dafe0f`  
		Last Modified: Tue, 19 May 2026 23:37:51 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:73eeb0dd63ebec84da1c4902f55f2b09938f12cf1e44087992f28df3c08758a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abf22f4ccfd1c8c3f14f9b1c4f17a09a546731de7c1cb36e5bbc0e246e76215`

```dockerfile
```

-	Layers:
	-	`sha256:bd49b5263e7d09eb6adcedf9e31367575640e0e2377223e073333aa452ecf674`  
		Last Modified: Tue, 19 May 2026 23:37:52 GMT  
		Size: 4.0 MB (4006043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:919c4334588acaf0f15aa0266408f3adc00b993ba67ea3c0501caee388bdff1e`  
		Last Modified: Tue, 19 May 2026 23:37:51 GMT  
		Size: 20.7 KB (20659 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:dd700f28055b8f3d2cb8ec23afcae8a34ead3be465514a71731b4547a70cc8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66376578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ec60fd61a37396a497605e04b27349fc7eed153674bf77a4d3bb6b92b5c12d`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:49:21 GMT
WORKDIR /usr/src/perl
# Fri, 08 May 2026 23:07:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 08 May 2026 23:07:29 GMT
WORKDIR /usr/src/app
# Fri, 08 May 2026 23:07:29 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24acde6d1e4e16cbadc8f232a1dd36eeaecbfbd4bb1dfb725e5c40355d61459f`  
		Last Modified: Fri, 08 May 2026 22:58:33 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d63461fc7b6de0a7b0c0c0a63d9810e4cf3a607cd4e23553800fc7f6f111d38`  
		Last Modified: Fri, 08 May 2026 23:07:49 GMT  
		Size: 32.8 MB (32778222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238bff3a533db5a84dd628c5e77646e81cb605281bc75e33216fa29d083bbe08`  
		Last Modified: Fri, 08 May 2026 23:07:48 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:f62c7fb1b07d73f7aa0300279d2be1a7e210c091eccb8feddf5d81dbfa9c7e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4027429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8bf7ebdd23d1a4637bf513235808d6bd7515cb9b5f32c517917603856389cf`

```dockerfile
```

-	Layers:
	-	`sha256:091afc819546b8a471d3655e901b8ee447bf7efd7efc044cbc40afd40d6dcff8`  
		Last Modified: Fri, 08 May 2026 23:07:49 GMT  
		Size: 4.0 MB (4006866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8909f1d29c3dd4b3c7492191629b5ee463f97ea6c3ccf586025217dd902f657e`  
		Last Modified: Fri, 08 May 2026 23:07:48 GMT  
		Size: 20.6 KB (20563 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; riscv64

```console
$ docker pull perl@sha256:3b8ac187057ab5cee6714582900b43fc7888630b8f33adbb551ace1d19e4c3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68095392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4e2fe47b0b6599d27386ef41ab65dd9b2c50e8b5db86869f8152843295451`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 02:26:28 GMT
WORKDIR /usr/src/perl
# Mon, 11 May 2026 04:25:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 11 May 2026 04:25:30 GMT
WORKDIR /usr/src/app
# Mon, 11 May 2026 04:25:30 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2481e2aa640643fcb248bb32f0916ccf5ac884b5babbbcadbe4c92423293f085`  
		Last Modified: Mon, 11 May 2026 04:27:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66a172a3997d3dd490714a4098f88f3dde97f5afeb49dcfc2a557f85c5d4ec0`  
		Last Modified: Mon, 11 May 2026 04:28:05 GMT  
		Size: 39.8 MB (39814891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0620d8364a6ccbea1f8f039827c7ae22babbd942b39e406179debc5118c953f`  
		Last Modified: Mon, 11 May 2026 04:27:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:57f5c4527d955bfe3a98d5412543ed6b4c06719abaaba79173b6d8b1b5a80c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c6781f8e0f05eb005766b208355319ed944c5e0a2c61f8d8563149e11d5006`

```dockerfile
```

-	Layers:
	-	`sha256:68f54f051cab0f9bf2a04e25a2d997d4c619fef028f9537a93c829d764fcf275`  
		Last Modified: Mon, 11 May 2026 04:28:00 GMT  
		Size: 4.0 MB (3998132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f36813dcde20f8acbcfb8adc4db65cd513f9a9f113403346a96b23d579165f4`  
		Last Modified: Mon, 11 May 2026 04:27:59 GMT  
		Size: 20.6 KB (20562 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded` - linux; s390x

```console
$ docker pull perl@sha256:c29ada55a6d32e78e4d706ee5a18aeb9ccbf770c0c10a7f91abe511185c44c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61192564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6c3e5b04751e9c22ef3af4128a8952b6f6a11c1bea3b45b295a0f282863f9d`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:27:52 GMT
WORKDIR /usr/src/perl
# Wed, 20 May 2026 00:34:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 20 May 2026 00:34:56 GMT
WORKDIR /usr/src/app
# Wed, 20 May 2026 00:34:56 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8ad974183bbb2951a6e9525fe03eddce49e4a1213c3d32995e5e618ce277a4`  
		Last Modified: Wed, 20 May 2026 00:35:14 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04245d92bc011a7d29a1c9d2b1ae686aea903c6a9eddd95d14c5373650b3e655`  
		Last Modified: Wed, 20 May 2026 00:35:15 GMT  
		Size: 31.3 MB (31346374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdefbff3eba5b29c2f5551f895429119776472ac185869c6ddf9eb436538e4b5`  
		Last Modified: Wed, 20 May 2026 00:35:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:e5560ac1a466d8b3e3c45a7893466ddc46afe648a9bfffc73e44a1a60b8a3681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a0c3048813aecc9d60a9a2d4d98b1d46bcfe9c733caeaf9c4dbf247cc569db`

```dockerfile
```

-	Layers:
	-	`sha256:b94b723d98ae7afd9b164b57de2d74df203927c80d18162e82a3e8969eea7cf6`  
		Last Modified: Wed, 20 May 2026 00:35:15 GMT  
		Size: 4.0 MB (4003236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f685897544e943316c11bef2a344f0380f5ee807a3ee876851cc9b2d48acc4`  
		Last Modified: Wed, 20 May 2026 00:35:14 GMT  
		Size: 20.5 KB (20483 bytes)  
		MIME: application/vnd.in-toto+json
