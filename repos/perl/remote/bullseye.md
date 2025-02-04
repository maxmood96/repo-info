## `perl:bullseye`

```console
$ docker pull perl@sha256:d6d828d1fc0239af6373d2a3a7e21c9ba2c93efdf018560bdb6ca6a21e696b0c
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

### `perl:bullseye` - linux; amd64

```console
$ docker pull perl@sha256:63ccf805818fa0fc4be261245721f7315fcf24fadda253312252e753c6c7bece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336906780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d3e12e569c07a8270f790f27ca4606c00014421b183eb6e58497bea37d9d95`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.1.tar.gz -o perl-5.40.1.tar.gz     && echo '02f8c45bb379ed0c3de7514fad48c714fd46be8f0b536bfd5320050165a1ee26 *perl-5.40.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.1.tar.gz -C /usr/src/perl     && rm perl-5.40.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.40.1" "-de0"]
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 05:19:08 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d32181a1ed55cf7269c27a7a18858d7a4679d9fccbc616d5d878b6ddded25b`  
		Last Modified: Tue, 04 Feb 2025 06:14:22 GMT  
		Size: 197.1 MB (197072749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa079459822ac9280099362ba4122ad818ada481d90891ad544633ca86f073`  
		Last Modified: Tue, 04 Feb 2025 07:19:28 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dabfd7dcd84f0215c90db75de943feee7b21622411a14cb3524b18e6a1fa60`  
		Last Modified: Tue, 04 Feb 2025 07:19:28 GMT  
		Size: 15.8 MB (15784703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f203c5d5526b647d9777ef9808f9d84d89579ec3913a255027e6a9ce87c37ab`  
		Last Modified: Tue, 04 Feb 2025 07:19:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:4fec15e406a755c1b2ac733c7d3ae2a0b7a6ff1fa6280f7c4062b28fa2f852bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15091769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b96d34300e8cc36fe851b400bbc1562c07857f17800b2648cf015bab30c7ce9`

```dockerfile
```

-	Layers:
	-	`sha256:de3a0fb5b7db261dd84812c730fca2a22ce7aaf377dc9fdd8b3e3952b1cf391e`  
		Last Modified: Tue, 04 Feb 2025 07:19:28 GMT  
		Size: 15.1 MB (15073616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7358ef6b2ee7c1f10ae799e55e4161dad49631d12983e5ae1f4bdbf84ea0a1e`  
		Last Modified: Tue, 04 Feb 2025 07:19:28 GMT  
		Size: 18.2 KB (18153 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:e1a4f0f6044b51ae74fea54dd9f0162198dfefbbb3ead177238d270e4054a1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296739716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4809bc7b2aba463f4a78cf75dfeb951830098cae7ca8721cedacd66e498e86`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.1.tar.gz -o perl-5.40.1.tar.gz     && echo '02f8c45bb379ed0c3de7514fad48c714fd46be8f0b536bfd5320050165a1ee26 *perl-5.40.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.1.tar.gz -C /usr/src/perl     && rm perl-5.40.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.40.1" "-de0"]
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526075af1d9c0b728ff0e8888d46f79edd8fb9bacc975b1eb824b9bca2c06ee2`  
		Last Modified: Tue, 14 Jan 2025 21:56:34 GMT  
		Size: 167.5 MB (167525487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e4a92e71b155f8fe9896ed3812a2fd6d9e2029a8e82696c44717ec51f6680`  
		Last Modified: Wed, 15 Jan 2025 05:07:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e9d27f4823eaeeedc0ad242ff7d7c53f893f8c74c1ea6cbafccda1dabe1f20`  
		Last Modified: Thu, 23 Jan 2025 01:53:00 GMT  
		Size: 14.9 MB (14874422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc461e67140d59e45137fa189b733611b37196573daa1df65642c398eb6ae4a5`  
		Last Modified: Thu, 23 Jan 2025 01:52:59 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f5ff03d62a5a1a86be7ad5aafa38c6b82e35d2a9ce0b3477a4cbbddf06529486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14892624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4284e6b20f1139579a02bb8f6153131a8a605c07feff5dc97d233a1a9709d3`

```dockerfile
```

-	Layers:
	-	`sha256:06627317d5166745f5f50aca3a1b8874f3d045cbe0c77a0faec76105dd22659e`  
		Last Modified: Thu, 23 Jan 2025 01:53:00 GMT  
		Size: 14.9 MB (14874387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b25a761873df92bfb9da3a061efba03d1e10d26a62f971615de8a7d80df86f`  
		Last Modified: Thu, 23 Jan 2025 01:53:02 GMT  
		Size: 18.2 KB (18237 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:3b8d04e965a1cf8e307350a8f9abdb6cb86f56df708f4b8a341e46c632054e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328348731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b8c628c437a0b2965226f25800a3b20b849c927f703b6122ffe660d4091d23`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.1.tar.gz -o perl-5.40.1.tar.gz     && echo '02f8c45bb379ed0c3de7514fad48c714fd46be8f0b536bfd5320050165a1ee26 *perl-5.40.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.1.tar.gz -C /usr/src/perl     && rm perl-5.40.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.40.1" "-de0"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5936a36467e76a2d54993295f16ff38dd2c24f30cf89a1f83a922f2440b869`  
		Last Modified: Tue, 14 Jan 2025 17:09:53 GMT  
		Size: 190.0 MB (189980217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4b9ab80f66e24837140e850189db5d516f8cdbd29428ef81e4bd9dd2b521ea`  
		Last Modified: Tue, 14 Jan 2025 21:29:37 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd9ad9753e2acfee92f432374306a0b0824497ac28cc3749cfa9fa7f94ffe1c`  
		Last Modified: Wed, 22 Jan 2025 21:30:20 GMT  
		Size: 15.7 MB (15725492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbeb88dd9777267c7b561d45501167790f560725c36ebebdc94572aa86098bd`  
		Last Modified: Wed, 22 Jan 2025 21:30:19 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:90eada85aea5b8dfcfd169276824bf42d9c2be6b4362764f4136af2bba912efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15094137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231acbe4998662a439520d3e5eaaf85dad19a67dd4aa2e0b21206e8cf5c21757`

```dockerfile
```

-	Layers:
	-	`sha256:71a2a920f39f4a88aa5db40ca72edacbcaebe504d5d31f815c7aa234e39f8929`  
		Last Modified: Wed, 22 Jan 2025 21:30:19 GMT  
		Size: 15.1 MB (15075868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2575480522fef344237d43f72c712018ff1f8b79c0c7d83e7ceb637f3f44988f`  
		Last Modified: Wed, 22 Jan 2025 21:30:19 GMT  
		Size: 18.3 KB (18269 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bullseye` - linux; 386

```console
$ docker pull perl@sha256:e30c7c8eecf016255dcf88fbf68f5c3a3c8037a51fd317f08d9a781461fcc9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.0 MB (342036814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49af442031f5da7239ef5f5bbbb21b7d130b7370b8e996cafbc999eb723d228`
-	Default Command: `["perl5.40.1","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/perl
# Wed, 22 Jan 2025 03:53:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.1.tar.gz -o perl-5.40.1.tar.gz     && echo '02f8c45bb379ed0c3de7514fad48c714fd46be8f0b536bfd5320050165a1ee26 *perl-5.40.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.1.tar.gz -C /usr/src/perl     && rm perl-5.40.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 22 Jan 2025 03:53:54 GMT
WORKDIR /usr/src/app
# Wed, 22 Jan 2025 03:53:54 GMT
CMD ["perl5.40.1" "-de0"]
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 04:23:38 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e7fd9b17628990db3e961c2d7570421849af1fe255937c0a9e48cf49a48f`  
		Last Modified: Tue, 04 Feb 2025 05:15:33 GMT  
		Size: 56.0 MB (56029876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b370f45f01968d6de3175fc994cf545ece88435b9abc17f2ed4705ac128c8d4`  
		Last Modified: Tue, 04 Feb 2025 06:14:51 GMT  
		Size: 200.0 MB (199980423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad7cc5b948e36713fc81213c1dee5e796abb2eac04ecb2641cab0cdf2a425d`  
		Last Modified: Tue, 04 Feb 2025 07:20:19 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a707e35f31bc5ec0d7a82464861e28264503f9ccb1b29c75474f3780427fff65`  
		Last Modified: Tue, 04 Feb 2025 07:20:19 GMT  
		Size: 15.3 MB (15288241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11467391adde2a60f5f8f205a7bdd0edc69eace91a16bf2f2d6177461f3a67d`  
		Last Modified: Tue, 04 Feb 2025 07:20:19 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ff85de5b2c3cc0f04bcf373b94c2f1338fdebbb47b95c9ee23953ad0e382efeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15080057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f471642b298fb2efc64cc4390dca30b176d2dcead614fedb2bd3a2b89a64588`

```dockerfile
```

-	Layers:
	-	`sha256:5de4621a68c0fac46f32ad5249539bf8686a4722353296bc8b7296f85b86f74f`  
		Last Modified: Tue, 04 Feb 2025 07:20:19 GMT  
		Size: 15.1 MB (15061941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08321b3647b74fb8335330c9bd03852fc25de40bb151ebe51e2704efbcd5a76f`  
		Last Modified: Tue, 04 Feb 2025 07:20:19 GMT  
		Size: 18.1 KB (18116 bytes)  
		MIME: application/vnd.in-toto+json
