## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:51a2cae9b59b474a412bcafdf4b7fbca44d51439a9d369546e366a9e58d11c87
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
$ docker pull perl@sha256:6b94801a09830da7863312c8f6373c31bea5b6d8f4f5b81bd594a3a18cba124c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56779172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26b3d65f90e717394655716a0c0da1f5225710f9d998d1968e6527b2ec6fab9`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:28:43 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:43:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:43:29 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:43:29 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4238e2884ddf3ca7b394a909dac880515de0bee4350c84d3475445d854523959`  
		Last Modified: Tue, 19 May 2026 23:33:15 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562d1e567b6a5359d7db95f6239207db3f5481791bf7a9c1976e16afe1616d28`  
		Last Modified: Tue, 19 May 2026 23:43:41 GMT  
		Size: 26.5 MB (26521306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc897d9bd30ad1784a6b2188e7d308ef1243095c17dd08b3184943502ec82ee`  
		Last Modified: Tue, 19 May 2026 23:43:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2cd8a82acd22499194dfbffc9841c74d640d08fbef550964c9a01dd651283600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4147462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7b8009daa04b09aa6f23ce867bfafe567ff4d5c43116f37d210058f272fccd`

```dockerfile
```

-	Layers:
	-	`sha256:f1cb68fd83658853043021ef8efe22ebc6f56b5ce39bc8815c6268d481b2d2e1`  
		Last Modified: Tue, 19 May 2026 23:43:40 GMT  
		Size: 4.1 MB (4129117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e0a7df26ce96df102d607634c93146d3951f40021b79ce7a5753fb846ba4257`  
		Last Modified: Tue, 19 May 2026 23:43:40 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:a25e0275780d7d50cb5f3a91d757d231b1d629da468add575d612a78a427d65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49296232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2813ccb09dff0e74235ea1f392e500f03475cbd58aee6947d30e03ca93caae57`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:46:23 GMT
WORKDIR /usr/src/perl
# Wed, 20 May 2026 00:52:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 20 May 2026 00:52:16 GMT
WORKDIR /usr/src/app
# Wed, 20 May 2026 00:52:16 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:03d011f22c8996d930f4cd66e165f41f901636aacd59f9f3a74c6b0df7ffa952`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 25.6 MB (25550938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b301acf993c7e8d502169ce581fc4c6fd09544406eedda51d7a6e6d019a0f47`  
		Last Modified: Wed, 20 May 2026 00:52:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33909dd6969f49f211c8ffbcd0374c7be46b95dc9cdf68829aa0ee6e5548eb9a`  
		Last Modified: Wed, 20 May 2026 00:52:27 GMT  
		Size: 23.7 MB (23745027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98426674520794854d54758337c0109f12b0516105e3df4b6fcec6a9d62c54c5`  
		Last Modified: Wed, 20 May 2026 00:52:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:5128fc6d521f0a623fdea9022ff5031ba7a45a414380d25ae05b068b68cea79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f84ec7a6f7cfe9f2b1287c5629cd1452af0e870078804276e3a9697701e6cc2`

```dockerfile
```

-	Layers:
	-	`sha256:7c2ce26c4b14632a404954006759119dfdfc8084ee170ef04240ab6d44d4c47a`  
		Last Modified: Wed, 20 May 2026 00:52:26 GMT  
		Size: 4.1 MB (4103106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2591b62d3713baaaf0a24fbc56dcdfa093d1b00e03a71d1d436c082057e05090`  
		Last Modified: Wed, 20 May 2026 00:52:26 GMT  
		Size: 18.4 KB (18418 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:1ddbf01817dadba29fed95ecb7d27a67db1f48a7d7a02249020835de6e1ecca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54366704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5915cca07c619facb3dcc96247084c71fa84da45020afbc7a4f571bc3546fdf`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:42:42 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:47:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:47:39 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:47:39 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae490a0b734390617cbf30b6866523576c57fb30926d48b2b6b39c86de42d491`  
		Last Modified: Tue, 19 May 2026 23:47:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f072b4bf875c33ccd6f7a2fdd0ec95ca76498cdc68dfe744abc49cfeb2af9`  
		Last Modified: Tue, 19 May 2026 23:47:50 GMT  
		Size: 25.6 MB (25623463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e62603dbb2537fe55ef1eb78ad5ffe133620df61c70814b7a88bf12e246024`  
		Last Modified: Tue, 19 May 2026 23:47:49 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0afd4973da20468867345860511d12bcad3f8f13744600b4cfe8f9af9d57623a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b17fdeeaa2148386bf1761eaaedb1952ad303c6f4b2beda08849ecce7d3612`

```dockerfile
```

-	Layers:
	-	`sha256:93f7b5434704ce667ef56c285e23b82ee90aeb8a69f485dfe64174ac37a4bcd7`  
		Last Modified: Tue, 19 May 2026 23:47:50 GMT  
		Size: 4.1 MB (4103512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:366f8964623bfe1bde0efc71c9c41a2c3f3e64c4b4ef5674745586741c1fcea5`  
		Last Modified: Tue, 19 May 2026 23:47:49 GMT  
		Size: 18.4 KB (18438 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:893841bf3e1410fe99d19b4f49064be91348e9b1df8fe337276855a4d2a990dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59275578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4858dd09e554aef150910416d17e02fe9dc36e34b895feacf7985a8f7ced0c52`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:33:18 GMT
WORKDIR /usr/src/perl
# Tue, 19 May 2026 23:38:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 19 May 2026 23:38:42 GMT
WORKDIR /usr/src/app
# Tue, 19 May 2026 23:38:42 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:2f6471dabb4ec95bed651099aaba5ff48a4c6332742cc6af6c957b880b8a6aff`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 31.2 MB (31192759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be4235f3336ae4809e366f9ab98a7e7bd403b80cdc98c75b5405960a1ef1bb7`  
		Last Modified: Tue, 19 May 2026 23:38:52 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0258ee426cdfd30841b537f5595eb7c09dfebdee7e0dbb4482db9061322e6da0`  
		Last Modified: Tue, 19 May 2026 23:38:53 GMT  
		Size: 28.1 MB (28082551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2260602ab98d0ae43e78fcf4dd2625b64af9559e8f93a6ec216176e2d49767`  
		Last Modified: Tue, 19 May 2026 23:38:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:40cae88d557658e99df70828d5b232c25972d8e08580a1fb8f70352814777d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f049dd5653ced3757f0b8aea42f05e1c7693dae26a0483028302da0e693369`

```dockerfile
```

-	Layers:
	-	`sha256:ee625f31d563390132328ca4d45e5b079d09e79c8c92527403cfffe34d691aa9`  
		Last Modified: Tue, 19 May 2026 23:38:52 GMT  
		Size: 4.1 MB (4133399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:353b2138599f834fae29761818077029300c5d71c7b26bfd532bdcb768436659`  
		Last Modified: Tue, 19 May 2026 23:38:52 GMT  
		Size: 18.3 KB (18318 bytes)  
		MIME: application/vnd.in-toto+json
