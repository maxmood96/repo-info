## `perl:devel-slim-bookworm`

```console
$ docker pull perl@sha256:923e980e735f38254729c75d27a9d4d6bb47a3004352aa261c94f62a6a66fd45
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

### `perl:devel-slim-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:31f48a6cae89fb320c8b2049f6f7b0f6a62f161c1020889b2ba8481f7f41275d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58444919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8516db79dcf41969d3f71469262f4757843ecc84c8fae1db63bd28ab9f3644a5`
-	Default Command: `["perl5.43.1","-de0"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.1.tar.gz -o perl-5.43.1.tar.gz     && echo '5221ebf5badfbb943d168ff589ce93456a11f219105c930cc01e8a82a62adb65 *perl-5.43.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.1.tar.gz -C /usr/src/perl     && rm perl-5.43.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.43.1" "-de0"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060020b98927abdd2fda1bf811beb2123c65ab9c675d77c6790a4d40524ad325`  
		Last Modified: Mon, 18 Aug 2025 18:10:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4651d9d30554597ba954113c5b646c0e92dd217bb56573099c523e0f9e0382ff`  
		Last Modified: Mon, 18 Aug 2025 18:10:39 GMT  
		Size: 30.2 MB (30214396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb432ad4428900186e1b832fc121532ef47f9d9931301cd7492a59ddb725344`  
		Last Modified: Mon, 18 Aug 2025 18:10:36 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:3347c44c92873a521780390b67a02624a25413ac764c04d9422536d576c0a6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6544fed5f6f24edd33d129770a96983baf5e299c9d1dc01723c846fa45bb14f`

```dockerfile
```

-	Layers:
	-	`sha256:f428767029e5e795ce39fd3c0d5f8e1878a19a3f403e0d9a14a46f6f984f116a`  
		Last Modified: Mon, 18 Aug 2025 19:47:20 GMT  
		Size: 3.9 MB (3937215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9f835291670f81289da9807cbba1952b20042bc08fe564b0e74c791a3fdb41`  
		Last Modified: Mon, 18 Aug 2025 19:47:21 GMT  
		Size: 18.3 KB (18287 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:332b47a19a3c403d94fc39f8b6d94a7c242a9646b7861ba38e2c585079f349e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53048544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcf4402fb3e17fe09ae300cf895f561d18914ef18d33d7c2d6b5995ed863b31`
-	Default Command: `["perl5.43.1","-de0"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.1.tar.gz -o perl-5.43.1.tar.gz     && echo '5221ebf5badfbb943d168ff589ce93456a11f219105c930cc01e8a82a62adb65 *perl-5.43.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.1.tar.gz -C /usr/src/perl     && rm perl-5.43.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.43.1" "-de0"]
```

-	Layers:
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146752a9e897d66d698515c5012882014c92eb5ee3ee0d05222b55fbaa6d4a38`  
		Last Modified: Wed, 13 Aug 2025 00:19:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432dd2e056ee90b4689a6054fae2c5478ca3c9b0a7581ed5dc6871bac87ce876`  
		Last Modified: Mon, 18 Aug 2025 21:10:06 GMT  
		Size: 27.3 MB (27285558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff5a175cc46967fbf4a114053159af856c970078d21a4b0f59b58ce948a8ff5`  
		Last Modified: Mon, 18 Aug 2025 21:10:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:26126ddc28f912de9939d177a642571438761df020fee78a07c5d41510182c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3639911fb2d5fe6ac79e291db6953de7df9eadfdb568681276e4e5d45669b43`

```dockerfile
```

-	Layers:
	-	`sha256:7f62625e09aa65d88e215830c79129becb555ec1cae12e45f7e0b0e06f760812`  
		Last Modified: Mon, 18 Aug 2025 22:46:48 GMT  
		Size: 3.9 MB (3908066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1f97c3a1201055db03b8ecc2bedd1f84c74c294769bd3daa79c04f58526005`  
		Last Modified: Mon, 18 Aug 2025 22:46:48 GMT  
		Size: 18.4 KB (18355 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:cc6c7d533277d601574e6657e5a49d35f891a204c82f5ee1e2c2a8acfd41bebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50305321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9429b22950527413fca71157bde9266233cd026cd47668815a352ad7948f1594`
-	Default Command: `["perl5.43.1","-de0"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.1.tar.gz -o perl-5.43.1.tar.gz     && echo '5221ebf5badfbb943d168ff589ce93456a11f219105c930cc01e8a82a62adb65 *perl-5.43.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.1.tar.gz -C /usr/src/perl     && rm perl-5.43.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.43.1" "-de0"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2322ccce20f0016f59a4479bc74c8f9cb061f15bd5e494c8f6e8e9dd61b600b`  
		Last Modified: Wed, 13 Aug 2025 00:54:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af01f957b3eda8c20142d5f84968c6b75bbb16c374914f7b1d589f0ae9bba31e`  
		Last Modified: Mon, 18 Aug 2025 22:22:01 GMT  
		Size: 26.4 MB (26366124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d432c3acd9f393d81544c10dcb56bab025a3f573e263d2ae272b3c0d5fe4a79c`  
		Last Modified: Mon, 18 Aug 2025 22:21:41 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:b5df55c80fa21eaa79d51c4b1f78ed0546388c1592b1bd17eb2e4a6de3721348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b35e6a82356ae5066f6b19abff950187874b52de8ff9d2a52fb964d9e963dc`

```dockerfile
```

-	Layers:
	-	`sha256:a116215ae71104ad1018a13185405052d5f245ae9c8c219e18a0697bdb1d350d`  
		Last Modified: Mon, 18 Aug 2025 22:46:53 GMT  
		Size: 3.9 MB (3907291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9732d650dcb3cb97f08a9c8fc97dc61635746094f5eb115737a47760573eabf3`  
		Last Modified: Mon, 18 Aug 2025 22:46:54 GMT  
		Size: 18.4 KB (18355 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:2a0297b1d9c394961ef7b78b18f7d7b6877ef2865e09e9c7ef345afdff98aecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57142358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3990bfe3d053fb93d51f9afe90a38f93de616e9dd261389180e3f745a13bec4`
-	Default Command: `["perl5.43.1","-de0"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.1.tar.gz -o perl-5.43.1.tar.gz     && echo '5221ebf5badfbb943d168ff589ce93456a11f219105c930cc01e8a82a62adb65 *perl-5.43.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.1.tar.gz -C /usr/src/perl     && rm perl-5.43.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.43.1" "-de0"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d7dbc08f34b1f931163e14b58c70803884a22718586fbb9241b5896171ccc`  
		Last Modified: Mon, 18 Aug 2025 18:21:54 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67236c068a19026b8c4badf8ab32be49c6a112576f13e6b468e2b91fb97dbb92`  
		Last Modified: Mon, 18 Aug 2025 21:18:43 GMT  
		Size: 29.1 MB (29060089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58014d0d7fe4abd8d7c3b496e8d12f52e81fca804622deda6dd609761bde10`  
		Last Modified: Mon, 18 Aug 2025 21:18:41 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:cac5956598c6d1f32f0dc25a1bc22846c7a9569079a72797e84b61aa3992532f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8f5e3584b6af461aadbd12a831e43d6762aac823abb61a30d7115c7d7c687a`

```dockerfile
```

-	Layers:
	-	`sha256:a2281d096920defabbb5e56e07d6f1ec79e631e7d7fa7dbbcc4a859156bb0ff7`  
		Last Modified: Mon, 18 Aug 2025 22:47:00 GMT  
		Size: 3.9 MB (3908452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afa6c9c1d2054be99e260ceb77330f13d1847309c763c666de32311563ac41f5`  
		Last Modified: Mon, 18 Aug 2025 22:47:01 GMT  
		Size: 18.4 KB (18379 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:097bc5bd2830f6c8475875d131a5fe99f5b6cec9c586f0b285eb360e326caa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58549065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac6521221a4ada2f7bf4b4dc891d36c895b5eab01c48592347d56d7d10fca5c`
-	Default Command: `["perl5.43.1","-de0"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.1.tar.gz -o perl-5.43.1.tar.gz     && echo '5221ebf5badfbb943d168ff589ce93456a11f219105c930cc01e8a82a62adb65 *perl-5.43.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.1.tar.gz -C /usr/src/perl     && rm perl-5.43.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.43.1" "-de0"]
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab9b8da57143cd7f6ae7d4588b24767156f3e214a4e3c165264361605c3266`  
		Last Modified: Mon, 18 Aug 2025 18:19:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb9d91fb944bac752ac4dff82b11cd0dc2208b597cd23424387a036e17c2224`  
		Last Modified: Mon, 18 Aug 2025 23:08:08 GMT  
		Size: 29.3 MB (29336191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edcd36835ebd5e29a2c4f1952a387a2ded6af7d6a5e0cbd0bf72527817bc1ee`  
		Last Modified: Mon, 18 Aug 2025 18:11:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:01ea212801140e9e8c4c14fe6db487b90057a558af93ee833b8129eeb682600c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35009f0678121ddffe82e4859f1ea2e2e090a57f6dedb02fb5690132e6b8947`

```dockerfile
```

-	Layers:
	-	`sha256:44fd78be7934d8b46c7af7f68ab2bcefe7886adea65a7efa7a08e29316f3cb52`  
		Last Modified: Mon, 18 Aug 2025 19:47:26 GMT  
		Size: 3.9 MB (3931157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6393415c53954e8c42c990fd7de8ee24bf0af96d806732e51ddcd3c765539bf`  
		Last Modified: Mon, 18 Aug 2025 19:47:27 GMT  
		Size: 18.3 KB (18259 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:46f074d8d62c60884c40095d7008fe48b6574ec03cd7adaf9ada8c82d30c6693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56876967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0e7158b40d745e9fbafaa66f84200218d8333342ee117f1d65940d826a6a7d`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 04 Jul 2025 18:45:50 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/perl
# Fri, 04 Jul 2025 18:45:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/app
# Fri, 04 Jul 2025 18:45:50 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:83bd2d8e15bdca1c657f4e1229c9515648aa638816bf4ae6a4be5a7afaee3a81`  
		Last Modified: Tue, 12 Aug 2025 20:45:57 GMT  
		Size: 28.5 MB (28516923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d33da0c48d232122ba5e3b459be09f595e03bde969dd5bc007fccbd3a0c5f3e`  
		Last Modified: Wed, 13 Aug 2025 08:19:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8593c24f6679db7f3c916d138e27e8f04cc9c85d4173e3cf88cf0bed25b56a`  
		Last Modified: Wed, 13 Aug 2025 11:31:39 GMT  
		Size: 28.4 MB (28359777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17160e0757ea4287e6238b6f80311717e57c432c2525c5aacf174eaa9e51212`  
		Last Modified: Wed, 13 Aug 2025 10:49:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:8e99021416b4b24e662cb68bbe09e39cc25eb5fd2cd8fbcf96ccd2fe8fd3df0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957fee2bec0ddb12fcfcf57e0b4f6c8f315218000f4e08b2b4423452db456b26`

```dockerfile
```

-	Layers:
	-	`sha256:bb8cdcc750a9917eff6ffa378109c7093b8038904d7e978b8552a14999f1f516`  
		Last Modified: Wed, 13 Aug 2025 13:39:08 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:272227f0e3fa22746b423584de01ed32169294125525bfb824e8c58b1b83d1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63078476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654a7653ed1096933cd6753677d4d8de1a9c7912bf9c7a2d163df8449fb2ec23`
-	Default Command: `["perl5.43.1","-de0"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.1.tar.gz -o perl-5.43.1.tar.gz     && echo '5221ebf5badfbb943d168ff589ce93456a11f219105c930cc01e8a82a62adb65 *perl-5.43.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.1.tar.gz -C /usr/src/perl     && rm perl-5.43.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.43.1" "-de0"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d191148f8669c21adae168084e9b9c42b94e15eb261549dffb23f39c173f8aea`  
		Last Modified: Wed, 13 Aug 2025 13:16:35 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a35966dfb679b7b8e092ceed68bab2282320f134520388f313b8b81a651df0e`  
		Last Modified: Mon, 18 Aug 2025 21:19:16 GMT  
		Size: 31.0 MB (31004789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ced41363c4a9238d10f4b62e3f5227deb9373920f2a277c57e1c10bfa524459`  
		Last Modified: Mon, 18 Aug 2025 21:19:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:b7fbca5d0fcc332d1f81be7f832875f334eba5e3b032827afa1bf6dcbf2cf3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed81de4225b73e4409e2f7bf3d941b2e2235b1a94bd2e205b9425a46eab0c789`

```dockerfile
```

-	Layers:
	-	`sha256:0638b98e2d78864596d8df5c92baf53ca4e9bee4dad288910c757c1c1ef2b57f`  
		Last Modified: Mon, 18 Aug 2025 22:47:09 GMT  
		Size: 3.9 MB (3923143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42aa9f22501114f189b481906e878ddd895787a994531fc1f60465d83a80d07`  
		Last Modified: Mon, 18 Aug 2025 22:47:09 GMT  
		Size: 18.3 KB (18325 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:f93fafd32cb694aad3b425865cf703fa68ad2e85a26674f3fc8488b3233007f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55628933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddaa57128261d2516a35aa18a06d234303be0ba57de605e7451fa48a00701621`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 04 Jul 2025 18:45:50 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/perl
# Fri, 04 Jul 2025 18:45:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 04 Jul 2025 18:45:50 GMT
WORKDIR /usr/src/app
# Fri, 04 Jul 2025 18:45:50 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfa5cc136d2c75a99e3d0dce35603e43594a04be4f7a76e49da7b0c69b6f0c5`  
		Last Modified: Wed, 13 Aug 2025 15:25:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d231a567c3d0bbb357e32263a2b2db404b1d2d924c4f708180d53f0fd0de145c`  
		Last Modified: Thu, 14 Aug 2025 02:35:57 GMT  
		Size: 28.7 MB (28740828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545169f14bc2ef994923d8a5b990c5bba408cc0ce76be1e32b7ef252f7e859e7`  
		Last Modified: Thu, 14 Aug 2025 02:35:48 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:da7b0d04fa0c7cca1bc1e14132502befe48091d113facd49cb96c9e966787425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c1d41b96516c289032f9f08be0a6903cee6ca5e3bb62be22c80d63db5579eb`

```dockerfile
```

-	Layers:
	-	`sha256:30bdbc27e117e060ab42601589c49063ba2cfcfdc8b1f041e1e23ade9c18b226`  
		Last Modified: Thu, 14 Aug 2025 04:42:46 GMT  
		Size: 3.9 MB (3923400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4714539412aaf89e89d27ffd6a26ca6af9a8d2d19248cf551a136c0f2394f1`  
		Last Modified: Thu, 14 Aug 2025 04:42:47 GMT  
		Size: 19.2 KB (19183 bytes)  
		MIME: application/vnd.in-toto+json
