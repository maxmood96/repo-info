## `perl:devel-bullseye`

```console
$ docker pull perl@sha256:6d10fa1b99b28e791370d7b7fada241301c722cf5f1f81061a8796dd0847f9e8
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

### `perl:devel-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:8755ba46f07ac59e1d54188f795992f67c68a3f2429c903006b31694f3f38bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.7 MB (337715635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9275011fb15f230a748bab33f505b462ae4b10f7314fe4f199de52be23a48817`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:37:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:20:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:13:06 GMT
WORKDIR /usr/src/perl
# Mon, 23 Mar 2026 17:17:16 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Mar 2026 17:17:16 GMT
WORKDIR /usr/src/app
# Mon, 23 Mar 2026 17:17:16 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0ff4d4cf746a31c00387c43ae977fe8857c000814b13a0e845ac0ad9512cce`  
		Last Modified: Mon, 16 Mar 2026 22:37:31 GMT  
		Size: 15.8 MB (15790675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faec137085b3e3d42618e8e8e1e58ee7d0a106e862a2d903b6c184338bd17249`  
		Last Modified: Mon, 16 Mar 2026 23:25:34 GMT  
		Size: 54.8 MB (54760568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0ce93cf4af0a4d1b914449aeaf95a8e726b5e8a02586a2328cd76f9d782d4`  
		Last Modified: Tue, 17 Mar 2026 00:20:37 GMT  
		Size: 197.3 MB (197254545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b74dd22229e05c8c4aeda99df74de15236195d4935bcce68f7e6d8d0838fff`  
		Last Modified: Mon, 23 Mar 2026 17:17:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0aede97fcec26b91ffd11c57d617b1adbecc47b9b3a353090329277e062d6a`  
		Last Modified: Mon, 23 Mar 2026 17:17:37 GMT  
		Size: 16.1 MB (16147098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b55176e3120a75d990e7a5d8c4252cea63a710a9aaabb66b0bd173c4b640924`  
		Last Modified: Mon, 23 Mar 2026 17:17:37 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2b89351c73279272c1cf1835209df6b68b199fa55041bda15a654f277d7ebc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a89e0b2ac1d0a1f83559f2e02520e6bf2b286d5282d8aac03e5ee7143302a7`

```dockerfile
```

-	Layers:
	-	`sha256:9edd8c7ef9c3ce62bc2970081436612c239c7e27919d02d5e974de79e192d1c2`  
		Last Modified: Mon, 23 Mar 2026 17:17:37 GMT  
		Size: 15.5 MB (15472949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63b433a30a289edc3445e35fce2c708447e425fedc3732b14ad63c6ea7d11fd5`  
		Last Modified: Mon, 23 Mar 2026 17:17:36 GMT  
		Size: 17.6 KB (17605 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:14c7ba6aea3815d256e0e1abd5d01c0eb6ddf83547e91cfe79d047014721cc14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297553698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd75016151a22c28a02f3ae02074e8b0a7824fd0cc17a4061debb0c4f94c09ab`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:19:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:51:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:15:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:13:01 GMT
WORKDIR /usr/src/perl
# Mon, 23 Mar 2026 17:18:10 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Mar 2026 17:18:10 GMT
WORKDIR /usr/src/app
# Mon, 23 Mar 2026 17:18:10 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:3aff03d2e208bd4d9250a4b2e487bb2463ed0509ea4994969b2b335433f11faf`  
		Last Modified: Mon, 16 Mar 2026 21:52:43 GMT  
		Size: 49.1 MB (49053591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eaadeae5e8dca06784f6e8df6af3749f18ad9c2cad1d317604dc2d3b08d2fd`  
		Last Modified: Mon, 16 Mar 2026 23:19:25 GMT  
		Size: 14.9 MB (14905031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71032861fec9defe9e9c3f8070c31747665de1cb5a459771806bcec6df20a913`  
		Last Modified: Tue, 17 Mar 2026 00:51:37 GMT  
		Size: 50.6 MB (50641289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3be18ac290ed431d8a2067d0eca8e4cf68988d64e3e6faad664f2491154bd17`  
		Last Modified: Tue, 17 Mar 2026 01:16:14 GMT  
		Size: 167.7 MB (167728375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0c383ea7649756b1954c6a93f7a1de5ecd220dc22e0945c1673ced1ae507`  
		Last Modified: Mon, 23 Mar 2026 17:18:29 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1776623f9a6f8e3d37956a0c9a48a5914459b61930f4ed76cb20167380b6844e`  
		Last Modified: Mon, 23 Mar 2026 17:18:30 GMT  
		Size: 15.2 MB (15225145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a7ea08bbbd6570be54ddd37db60900cf84b642f2275bb705cfa0226bb4abd0`  
		Last Modified: Mon, 23 Mar 2026 17:18:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:df16e7feadd595da92337a4fd9228ad52012ec6aeb6d6f18701a48e2c865ce90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15289953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f973d251653e4cab52a46d2f1ab5b9e67d3286cfd7f849ec2805d59eaee85d`

```dockerfile
```

-	Layers:
	-	`sha256:3d39bf053fd429f45fcb76e811a6ad41cc51b8db32a5b324c474eb6afb8d286a`  
		Last Modified: Mon, 23 Mar 2026 17:18:30 GMT  
		Size: 15.3 MB (15272275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dc838d748740385c707bd0c39740fed0195bdf0865631a73502729ffb970ec5`  
		Last Modified: Mon, 23 Mar 2026 17:18:29 GMT  
		Size: 17.7 KB (17678 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:b38a4f77e2ce1ae1c0ae0625d3abe527022e0263e3c17971416b222cfb916bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.1 MB (329141541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6541340b9894c3124bb70fd6088dcaa98fd826ddedd5042911ab92d804c844`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:13:18 GMT
WORKDIR /usr/src/perl
# Mon, 23 Mar 2026 17:17:40 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Mar 2026 17:17:40 GMT
WORKDIR /usr/src/app
# Mon, 23 Mar 2026 17:17:40 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84fbb63fb33355ef8feb355101d06b509baa6abddd911e5e232c23e80b5d767`  
		Last Modified: Mon, 16 Mar 2026 22:39:50 GMT  
		Size: 15.8 MB (15774783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb6d461b58cdd0c5268a71ddb9eec2ce4959e3487059981d8117b3069138ccc`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 54.9 MB (54874988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12eccd521fe266794ef8a5e3de047b94cd53cc118b8e4ec8920cf3f9a3b498a`  
		Last Modified: Tue, 17 Mar 2026 00:20:30 GMT  
		Size: 190.2 MB (190173282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7006550302113be526da28bb6d5c8cdfa67b5f2e601e0a24fe0933cb058581c`  
		Last Modified: Mon, 23 Mar 2026 17:18:01 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988296e1ce815c92a4a446e7885c5d09786db330cbd31d1f7ecf38460d0bb303`  
		Last Modified: Mon, 23 Mar 2026 17:18:01 GMT  
		Size: 16.1 MB (16070969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85d74577e31ebb2bbad8f49908a9ed4fbe6eb8bf4dceb20b0127605f310f744`  
		Last Modified: Mon, 23 Mar 2026 17:18:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ae2fcda61965e956c88ba2e68be364b9b267a75fb71bbd05c0b1fb7484b28de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15492604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205733be2a2642ef13f900a1e741cc80bb867718ac1b5f83b873a716d526381d`

```dockerfile
```

-	Layers:
	-	`sha256:3a1774f7a2eaed0245aa2a14ab22b7e8212bdb51f67335d65673e52c3eac9b37`  
		Last Modified: Mon, 23 Mar 2026 17:18:01 GMT  
		Size: 15.5 MB (15474906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77ca116bbae157caa43f26220b9b98c2662cdcd6aa4e05dc9f193b43788518f4`  
		Last Modified: Mon, 23 Mar 2026 17:18:00 GMT  
		Size: 17.7 KB (17698 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; 386

```console
$ docker pull perl@sha256:00fadc2e4b9331177a035fc305c524eb5d5fd1154b4fc3ac0d1cfa1434ffd9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.9 MB (342869975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5d6e5a465291a38f431064aebecc76ad1e77adc90b43602b6f19debefb9253`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:43:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:41:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:13:18 GMT
WORKDIR /usr/src/perl
# Mon, 23 Mar 2026 17:17:55 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Mar 2026 17:17:55 GMT
WORKDIR /usr/src/app
# Mon, 23 Mar 2026 17:17:55 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:ad236c87f3ff6b413233974bf5899e332a9ceee3a606736011b98ba6596c59ea`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 54.7 MB (54702245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acfe19e42191cd08e20b1140d1c12d03ada06096409a1802c622395bda4436f`  
		Last Modified: Mon, 16 Mar 2026 22:44:04 GMT  
		Size: 16.3 MB (16295580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dff001bd2ae96d5b52e166c1481e29711d5ecb13cc3d257a5152666de3e84df`  
		Last Modified: Mon, 16 Mar 2026 23:41:46 GMT  
		Size: 56.1 MB (56059192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df870ec330a087681f22cf47f4c5ed1d637647f6c9bbe723e86ad18b3eebc16`  
		Last Modified: Tue, 17 Mar 2026 00:20:24 GMT  
		Size: 200.2 MB (200172892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4296069458f6b31b44d525f29c9be0fd925dff4f4573018922c646779bc28c`  
		Last Modified: Mon, 23 Mar 2026 17:18:15 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc126268c3a1317450ebf6e3fb6514cdca15a6386336961588ca23cfb1df5606`  
		Last Modified: Mon, 23 Mar 2026 17:18:16 GMT  
		Size: 15.6 MB (15639799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a256e47ee50152604ea375e34ce36b91ce0cddb9264a535f9607c7c37c01fd`  
		Last Modified: Mon, 23 Mar 2026 17:18:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:9e7f2e7b98964b70a88550c069b84be033ed7f63c3f96e9e029024fd0e3ca294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15478538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3980705904b3650732c2715f080111ec0e6b5a92c68b1ee6f2b5f16885bec5a`

```dockerfile
```

-	Layers:
	-	`sha256:f8de2bb4363b9d375777b1ace2c60e2e0295a516fa8004944b7a8bb80d2df1f3`  
		Last Modified: Mon, 23 Mar 2026 17:18:16 GMT  
		Size: 15.5 MB (15460959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc33cbbbb95d1c8210b49ef710d65ec43ba0e34afd98fa96c24af37811f790b`  
		Last Modified: Mon, 23 Mar 2026 17:18:15 GMT  
		Size: 17.6 KB (17579 bytes)  
		MIME: application/vnd.in-toto+json
