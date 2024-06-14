## `perl:5-bullseye`

```console
$ docker pull perl@sha256:f96b0cbd6371fa61384c9251173c2b6a9fac787cb194c9afb2efaf8f449faf99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `perl:5-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:46d93a071ab57d5c80ee4e7366ad40c25c81822378202acbf135249a969eb991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338418077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2174adc9c3391518aee4a2746a0d7e5f78cb1ff8138aeedb9a40e815da672009`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065842589d7a62a96a08c1acc0bf9e7c0b5442f2770276be18328b755d1ffb99`  
		Last Modified: Thu, 13 Jun 2024 03:50:44 GMT  
		Size: 54.6 MB (54589356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbd10f967df496e6665aeab3e08f15f3d577c1489dbddc64908dc6bc9a22972`  
		Last Modified: Thu, 13 Jun 2024 03:51:15 GMT  
		Size: 197.0 MB (197017260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4410fb7b587c9f5c402386dcc03dce4883c929c514cd7f4b224bd639f9d51a`  
		Last Modified: Thu, 13 Jun 2024 18:36:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7d789c9e7f80fcbd216c7166e06987e9d33308b9aeadfe6b747a8ae72dbc76`  
		Last Modified: Thu, 13 Jun 2024 18:36:44 GMT  
		Size: 15.9 MB (15947170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daba778c550af7cb5b4bff3e04ea35f9225deaed8ab43a5c20e2a52cec1e8f3`  
		Last Modified: Thu, 13 Jun 2024 18:36:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:68dba20e5051e5fbd8fec80dbe7440990fdea3c8d14ea912c5981da43f0c56ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f342e673887a45564a3f72da44c6c13d0be04edb42382587d5e57699c3db7165`

```dockerfile
```

-	Layers:
	-	`sha256:f5959b214182c8f2f184cb0f660d6e5abcf3816cbee16859aa001f9082e02865`  
		Last Modified: Thu, 13 Jun 2024 18:36:44 GMT  
		Size: 15.0 MB (14974537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25e9b9aa1e89ba41d0eb6851a1646e2ea1bdc7a7f65d19463ed85285b4f85df`  
		Last Modified: Thu, 13 Jun 2024 18:36:44 GMT  
		Size: 15.7 KB (15689 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:7f802d589f8a5f493cc9db1c7f4667a3fa317d7601fd8bd5d2d45b6f4af8b0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310759055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577d4ea2c87f812e94c5a97b3126c9aaae5321c3bcbd59de521cb34d91a64b2e`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:e9d8f0f7fb10978e8599b4d65173747a249b36470beb002a75b03faf3b15e953 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:257495c53b4c673d8b6401bad898f12d6b9f0119d3414c2dbb1f82162a4269c8`  
		Last Modified: Thu, 13 Jun 2024 00:51:58 GMT  
		Size: 52.6 MB (52603036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dab18c03b4e38a2ea5387c0c9555851665f0b0944f448e887d01fddba91d24`  
		Last Modified: Thu, 13 Jun 2024 01:25:17 GMT  
		Size: 15.4 MB (15376071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cab5068a9c028c7944d8c796ef2a3f2f0405e6777b233048bc9107bb87a65e`  
		Last Modified: Thu, 13 Jun 2024 01:25:35 GMT  
		Size: 52.3 MB (52330351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e44e3b2454499d7c1424bf7ddc4cd476d1413aa087ad671dd79a68e82543870`  
		Last Modified: Thu, 13 Jun 2024 01:26:12 GMT  
		Size: 175.2 MB (175214715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79adfd54f967f1f68e871c1f891ec365961d42231334b212c2a8803ce78b753`  
		Last Modified: Thu, 13 Jun 2024 16:00:38 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11511ad7abe724be668e7ea5d6720e309b6d2ecdf36d974b95d0b231fdbe773e`  
		Last Modified: Thu, 13 Jun 2024 16:00:39 GMT  
		Size: 15.2 MB (15234616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c203c426342c5e4fbb902e6d5f30f8b7812b9a15660c617e3ef0f701aae75f9d`  
		Last Modified: Thu, 13 Jun 2024 16:00:38 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:cc139cdb5a236dbc90fc278cb10bf547eca6f30820427f63fef6c672cfb512b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14786822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cb4195ca94bdbe77221a5eac92c0aed52c79718006f5f0ffbf0e79dced4f01`

```dockerfile
```

-	Layers:
	-	`sha256:89e37db92611f1d1188426de663270fabe17f7cb85d70e1c299c8ab22c986012`  
		Last Modified: Thu, 13 Jun 2024 16:00:38 GMT  
		Size: 14.8 MB (14771056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:259957d55dbd28356b199e6a883d883bbbb887ca11ef4fcc4c8b26bfaf9e57ae`  
		Last Modified: Thu, 13 Jun 2024 16:00:38 GMT  
		Size: 15.8 KB (15766 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:f17638582fc862fc40167cd0036667769f2debcf9b6ee21e43aef10348280c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (298002357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e871aace1508c15978f63b92c33624426eae354d33b0a5950f6e303ba1b7d2d0`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738fc6141957592e4d069a8fcb0615b3f6dd757c25ee58dd7023fb923a7a4ecc`  
		Last Modified: Thu, 13 Jun 2024 01:34:36 GMT  
		Size: 50.4 MB (50359459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d33379b30e1ceb9b87b34482bff5906df43a22892099a6815c383a940044f8`  
		Last Modified: Thu, 13 Jun 2024 01:35:16 GMT  
		Size: 167.5 MB (167479604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ca553d13aaeebcae6f6a374742921a338e847127745903df200e64c633d2aa`  
		Last Modified: Thu, 13 Jun 2024 20:16:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0921568fa6afd3cec4c441a1fe6fe8036868752944c5ae5244e1ea532cceea53`  
		Last Modified: Thu, 13 Jun 2024 20:16:33 GMT  
		Size: 15.0 MB (15026429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbf741bfc51abac987535c6ad2e7d0ad4243f673107171fd205394cb309fbb0`  
		Last Modified: Thu, 13 Jun 2024 20:16:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:56289c76cc95af0dbe33f8dc345514bdba80838a19ce40fba33c5ed5298445f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14792196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d0495f2b4d4e3e384405e5e58d9ba394b6a57e5dfecd3ddcea34038442d332`

```dockerfile
```

-	Layers:
	-	`sha256:3e632b36fa3de47190503d2f74a5e8f138c6e6bb3f142e395029fe0b4d9c282b`  
		Last Modified: Thu, 13 Jun 2024 20:16:32 GMT  
		Size: 14.8 MB (14776430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0110ace4eaba2743c08a8883719a9679fd38b81558c65727d32f0471d58487fe`  
		Last Modified: Thu, 13 Jun 2024 20:16:32 GMT  
		Size: 15.8 KB (15766 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:a0abd0128a0f33b1d24fa7051dbb4f37b165a6886dfcbe51b21beb9a2c6f7619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (330004212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c132db35b9756c5befdeaa8cdc94f382b82d8962c6ab15e675b281e4c7d3420`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a7ca076c1ea04622ddf9f43ff2f138f6c50a40118747a45d2618cc64591d6b`  
		Last Modified: Thu, 13 Jun 2024 01:31:29 GMT  
		Size: 54.7 MB (54696375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315e6e292ef6ca0113f94dbf806ecbea714420b97b385d4138e3cb84616995e3`  
		Last Modified: Thu, 13 Jun 2024 01:31:54 GMT  
		Size: 189.9 MB (189935383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674b88b0552758c71c182855d703eb34f12c240b71ee740345b7abd7e5b08457`  
		Last Modified: Thu, 13 Jun 2024 20:12:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876850a4833ea2d85ae4979449666d9c803499b028a5fffcda6dcd0053ebb1e8`  
		Last Modified: Thu, 13 Jun 2024 20:12:14 GMT  
		Size: 15.9 MB (15882140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d24c2bdec913596ed3f452605b4424f75e32a0920ccb68f669f25aa4852429`  
		Last Modified: Thu, 13 Jun 2024 20:12:13 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ecab47c7015221ff4d2f6c593777fde4bc3aa5f1cc62d91ef06537b73f5c2596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14993071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1991f0394d64f93128ae1ce265578b5ceb73711fb386b644c3449edb5c9bb661`

```dockerfile
```

-	Layers:
	-	`sha256:d7a65ceeb92b0b0553b1925a688b244c00cd6d128c6b13673e730b99a6b9b7ad`  
		Last Modified: Thu, 13 Jun 2024 20:12:14 GMT  
		Size: 15.0 MB (14977058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae557eed3b08384c866814e05a309a2df90b2e758c5a7662359c3d6c6ee6da8d`  
		Last Modified: Thu, 13 Jun 2024 20:12:13 GMT  
		Size: 16.0 KB (16013 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; 386

```console
$ docker pull perl@sha256:ccecf3422f1b434bf98401ebf934d429b2e22099c5a3d336c9fcc437d0b3ebbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343636108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132622ceedad91e86075eadaf14a5c344397e87add153be2b1a66ab9f3e1f471`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b98f88bb530423206e6a932f7a0f7e81cc72458b59be08bcec8aa0490df79e`  
		Last Modified: Thu, 13 Jun 2024 01:20:13 GMT  
		Size: 16.3 MB (16268880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4e6f3cca702057a7a6cdbd9b2d2f758e1d85524fdc9fc26824db70376bce11`  
		Last Modified: Thu, 13 Jun 2024 01:20:33 GMT  
		Size: 55.9 MB (55929392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4267f96413a024e086769e096a862097360934db8c089f130cf1a23d340ab836`  
		Last Modified: Thu, 13 Jun 2024 01:21:16 GMT  
		Size: 199.9 MB (199918065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c5e1abdeb3338cff23e734429d9be3ec8d2db7668d43e515aa8c9907a8dc18`  
		Last Modified: Thu, 13 Jun 2024 02:07:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ca415de60de35b46bcd3dd4b10bf6328de40fa517cd006fc22667c4af3720d`  
		Last Modified: Thu, 13 Jun 2024 02:07:47 GMT  
		Size: 15.4 MB (15442965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024c7af6b51e0936309e3161131c5a0f49a7a95493cdc9a62b7c812a243b1817`  
		Last Modified: Thu, 13 Jun 2024 02:07:47 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:13e4d41e0f98b5805741143baa86504d68e60876fcf4ed9495a20ebcd9510781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14979016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f95bdb194a07563d30e8a3b0f70c6667e4a64bea0ad03980b30d2197828043f`

```dockerfile
```

-	Layers:
	-	`sha256:96e7f1958b55fcdb703f48c92952178174ee919e4ed56e6d00c2a9cfe53bef3c`  
		Last Modified: Thu, 13 Jun 2024 02:07:47 GMT  
		Size: 15.0 MB (14963361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c02b6dd2d29710b20f059b710b1a50e9a09afe30440252904b5537be914b180`  
		Last Modified: Thu, 13 Jun 2024 02:07:46 GMT  
		Size: 15.7 KB (15655 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:0398014fac50adbf9b7306c3149199fa973f7260fd86ee2c0cc64b2a99e06bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.4 MB (316447626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a779454dd51921175a1111a9e2b96c971133604ce1ae936565235565de74e2`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:2fd9c13efc7b13ca68928f53acc0c79d5841bd49e5aea46b2e1906120bba2a4f in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:6c9f7b7d6baf92c8cec25b325ea14db33b8c298218a5bcd368bb24184c5645b6`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 53.3 MB (53322503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f62fa3097190d71f8c07279b0414992956a17136d2040113e1f4910937c092`  
		Last Modified: Thu, 13 Jun 2024 02:39:25 GMT  
		Size: 15.5 MB (15530528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd553a7e4abf06bba101ca3a36c88140dd098954e94bafce76ee81b84c8c57ea`  
		Last Modified: Thu, 13 Jun 2024 02:40:14 GMT  
		Size: 53.3 MB (53313183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8887bb880586f84516d57dd8a975838495ce2ed3fa784f98ca887832dd72c4f9`  
		Last Modified: Thu, 13 Jun 2024 02:42:12 GMT  
		Size: 179.1 MB (179135669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3473e4f3aa2f40752b7b841703da66cc59afb40915c41d50b9b9bd5dcd1aecf0`  
		Last Modified: Fri, 14 Jun 2024 02:02:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700bfb71a5c9fe6e52b57dbd139399c3fba0f96460fcc033135032e9701b3e04`  
		Last Modified: Fri, 14 Jun 2024 02:02:20 GMT  
		Size: 15.1 MB (15145475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88988976e8e493ed2972fed94f6560d7d68f4d21366cbeb29f191f31a4050efe`  
		Last Modified: Fri, 14 Jun 2024 02:02:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ca700e4fa2714a43c4373b2d6c2d009a66341bf07748cf449840e1fe040f1c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce2c100ecd2b3f114dc87d5a75a5a59352b39ef70157a5fcf4f31e9a2af7016`

```dockerfile
```

-	Layers:
	-	`sha256:1b1928f8f4e4660a2e607f1c20d89822012810d89326f81d6e5b3ec98b33dcf1`  
		Last Modified: Fri, 14 Jun 2024 02:02:16 GMT  
		Size: 15.5 KB (15536 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:4c226a93e206ec0d82f0351c8cf8419293489d729438d4cb8a7f12107369b4e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.9 MB (346915531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27ad4775ee60814e7406ffd028e8c4c805df7cd22085d5cc49b5068dea710f9`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:32733696002797fb377d3d8094c21c0f41f25da6f371eb4a8ecb6fa5c3ef1048 in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:7afd12f588c414c122b8d3022d60effda2738a394347f5b3cbdebfe1420a8bf8`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 59.0 MB (58968957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918a353cdc3445173a18fe2f058dd7abb46fe3acfde05a65233cd1b979bd3d09`  
		Last Modified: Thu, 13 Jun 2024 02:01:07 GMT  
		Size: 16.8 MB (16766853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44a70314a2227a3d4a36c3baefe93d6e718bb4dd984f85adc8cb091a68f88b3`  
		Last Modified: Thu, 13 Jun 2024 02:01:25 GMT  
		Size: 58.9 MB (58874053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719a9ab0cabd6aa0929d32efa72a27e1b7732e1c13c57af740a74747a17626bb`  
		Last Modified: Thu, 13 Jun 2024 02:02:00 GMT  
		Size: 196.4 MB (196370976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbeb67d8944ebf0f06306374494537cbf7a045ab905c36973eb9a4fd07daad5`  
		Last Modified: Fri, 14 Jun 2024 01:28:03 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea9669a65ea6bb4c9b6690ae9f297b358b9ca8bae8b3ea9c2bc9f5a7494666e`  
		Last Modified: Fri, 14 Jun 2024 01:28:04 GMT  
		Size: 15.9 MB (15934424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527031988c19c263915d15cd970a02c01cb244f79179b260adb15712a80d170e`  
		Last Modified: Fri, 14 Jun 2024 01:28:03 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:5a17250587eb9eeab038e68432486a710eeaf833f24300af80f5f0377f4aad49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14959579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda7c7ca3ae051c0a9ced85a0068748c91a26670ae67196a19c7d2dacedfdefd`

```dockerfile
```

-	Layers:
	-	`sha256:d2c92ee613b32c8a4c058c9c9d4d11422da92e20204cff76fb610efaf00e7b16`  
		Last Modified: Fri, 14 Jun 2024 01:28:04 GMT  
		Size: 14.9 MB (14943846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d5433d13d9018b6b90a06dd552818e65388cfe9ff3986590966859c0da72e0`  
		Last Modified: Fri, 14 Jun 2024 01:28:03 GMT  
		Size: 15.7 KB (15733 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:57602617173f4a03004144de9d62fe2abfdd0ab6e2c3797b94dc7486bd406ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312375623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d10b3d3ec18aa90e45bd8df4ff163b077d2dcadaf8682bd23ba48deb2d2a03`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:42:51 GMT
ADD file:a0baaba4b04b93c49efe9fdafcb2308d4f775370b8e2a926df265487484d9788 in / 
# Tue, 14 May 2024 00:42:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:23:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:43f368780ca3724d6cdfa64641264541097ebb1b158cd3e0439fbf1846f179e9`  
		Last Modified: Tue, 14 May 2024 00:47:50 GMT  
		Size: 53.3 MB (53337573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a81dfed6865ecaa40f3f43b4bd4c389449dd3e0fcdc04d95ffd4c8e09fa9cd`  
		Last Modified: Tue, 14 May 2024 01:30:16 GMT  
		Size: 15.6 MB (15642393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0bebc382626195b064b7bc5d045ae9224b0d8f3c00157347449a593b555471`  
		Last Modified: Tue, 14 May 2024 01:30:30 GMT  
		Size: 54.1 MB (54076843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c7ec963ac714a2f94b076f8e287270d7deb6f725c170e54c73463524ff8f0a`  
		Last Modified: Tue, 14 May 2024 01:30:55 GMT  
		Size: 173.0 MB (173025883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fd97bd50f4e88f8002a7750cc8d78620ca6e3033ef42f0d7faecd1bd58f2b7`  
		Last Modified: Mon, 10 Jun 2024 21:17:42 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d1c85d6325079ec2f4be23793e06c7979c94ab824074b9784f0076ac034f36`  
		Last Modified: Mon, 10 Jun 2024 21:17:42 GMT  
		Size: 16.3 MB (16292663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7c84e063e3a519c1616ccf08fd29004b18594f08ec304cc30c3fa21164b435`  
		Last Modified: Mon, 10 Jun 2024 21:17:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:254294f7568c00d4003cca085c96aa7b2f854442833a74948f5926d7d7b606b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14811898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8349fe142c530bcaa5e6bccef8468bc13afdfbd92c74eb4531f7fc63f99b53d8`

```dockerfile
```

-	Layers:
	-	`sha256:379ffc876edc801e8e7d1ae61aaf47c62a917535edab9819493c8110d33ceead`  
		Last Modified: Mon, 10 Jun 2024 21:17:42 GMT  
		Size: 14.8 MB (14796209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0529669f412ab544f9e87581e09dd48607c7092c90c1c6f6d772584fc8dfa35f`  
		Last Modified: Mon, 10 Jun 2024 21:17:41 GMT  
		Size: 15.7 KB (15689 bytes)  
		MIME: application/vnd.in-toto+json
