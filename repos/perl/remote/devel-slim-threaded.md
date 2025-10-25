## `perl:devel-slim-threaded`

```console
$ docker pull perl@sha256:e9a2328ab1e36bcb0a84d445e2cb2592aeb3b547021c360466d7efa9adc0f010
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

### `perl:devel-slim-threaded` - linux; amd64

```console
$ docker pull perl@sha256:1e7bf230e3a3b3c1fd7633e62411424e62563ee7d8e1d4a0fb31fbc33468e71a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61912811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e3c7a58298c0dbedfaa301e7af4abd01850136b7bc5861c12f0d05b0a75f53`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/perl
# Fri, 24 Oct 2025 07:13:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.4.tar.gz -o perl-5.43.4.tar.gz     && echo '75676cc02c1d4d6f4577f7fd953e07ab5d06f71cf4201753ab6e2b0ddb5a4931 *perl-5.43.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.4.tar.gz -C /usr/src/perl     && rm perl-5.43.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/app
# Fri, 24 Oct 2025 07:13:41 GMT
CMD ["perl5.43.4" "-de0"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5834da2bcc02c707856a587adf271ffe0209b4c22266827d02ab518c12b301`  
		Last Modified: Fri, 24 Oct 2025 19:47:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25e5be063bf70fb4d5c853bffedafc590dce0cffbbd66af959579204f02e662`  
		Last Modified: Fri, 24 Oct 2025 19:47:57 GMT  
		Size: 32.1 MB (32134620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d29b44e68fb338543564b7af6d94695176133bc43adbfb3970a5841a53549a`  
		Last Modified: Fri, 24 Oct 2025 19:47:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:edceafc71ee2a97a700f34b6beae4496ddefde544f9c32f555047ea6c12626c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7407f6dc54f53482140ec88546c6eb61dbfc6bbc6746ae36eaa9624bb01dd3`

```dockerfile
```

-	Layers:
	-	`sha256:7c6317abf8677100910638ee56f583ee191540e515612e78a3f408bc0a38d285`  
		Last Modified: Fri, 24 Oct 2025 22:47:15 GMT  
		Size: 4.0 MB (4009358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d822516c207212707e28064ae1b6abd23b39faa9f9c2b7de15c8be9bb94d9d7`  
		Last Modified: Fri, 24 Oct 2025 22:47:16 GMT  
		Size: 19.3 KB (19331 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:14eef0f0916af0048ecc5e5dd4b74caac30cb34999f82fc8771a22ffd62774bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57297428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa6b3fbb8ad6c7d26a84a855194d1c64a16e1c8fb62a2b6440c2b1ad0dc815a`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/perl
# Fri, 24 Oct 2025 07:13:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.4.tar.gz -o perl-5.43.4.tar.gz     && echo '75676cc02c1d4d6f4577f7fd953e07ab5d06f71cf4201753ab6e2b0ddb5a4931 *perl-5.43.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.4.tar.gz -C /usr/src/perl     && rm perl-5.43.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/app
# Fri, 24 Oct 2025 07:13:41 GMT
CMD ["perl5.43.4" "-de0"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c94853f94171a0e2ff688fb3a048b82fef1a75abf5bb34e58d9075d3f854896`  
		Last Modified: Fri, 24 Oct 2025 19:23:03 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694c36a0b0c6bce301a1e23026b0c50b9ab09485c3aff09ebde6116490c7796d`  
		Last Modified: Fri, 24 Oct 2025 19:23:04 GMT  
		Size: 29.4 MB (29350879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1c105f5a4afb4672ebc7ff876faa2bb10471360601221c9cc011022eefb00c`  
		Last Modified: Fri, 24 Oct 2025 19:23:02 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:d2ce1c0e59170acd0f4fd127a7b76c6ce6dd22daaa02a89eeefe765dc5ee40a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d83fccf7051d99f40dc13b7bb59e57d7da2ba62d68a7da6bc60016f867e60a`

```dockerfile
```

-	Layers:
	-	`sha256:c2b9beae2dd44f33da62ec2ef584bfe7966d448728ab73f52879833443bac83a`  
		Last Modified: Fri, 24 Oct 2025 22:47:20 GMT  
		Size: 4.0 MB (4002403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a5e33d6a9f8c9cf81575b17c27c367984b45f73dc2289125f644b94645d2553`  
		Last Modified: Fri, 24 Oct 2025 22:47:21 GMT  
		Size: 19.4 KB (19427 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:72a0d12ad0735b92c55eb85689e7190d283fd2505fda0a9206e1ad60d4af1413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54636832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac97fcd516e258b1d418c5e5cc7714fd87617d94f4c97ecdb72b9446d07aa2a0`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/perl
# Fri, 24 Oct 2025 07:13:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.4.tar.gz -o perl-5.43.4.tar.gz     && echo '75676cc02c1d4d6f4577f7fd953e07ab5d06f71cf4201753ab6e2b0ddb5a4931 *perl-5.43.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.4.tar.gz -C /usr/src/perl     && rm perl-5.43.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/app
# Fri, 24 Oct 2025 07:13:41 GMT
CMD ["perl5.43.4" "-de0"]
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b77f2500aaf2102e642d933e9857d3922c231d53c44ee1403dc92aed55be714`  
		Last Modified: Fri, 24 Oct 2025 20:37:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f0ba5ae7e1c3790f244a12f94803a377e0e7e2580557726a59b19157b1ddcd`  
		Last Modified: Fri, 24 Oct 2025 20:37:40 GMT  
		Size: 28.4 MB (28423671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e318fe611ad342b03c9a845fcae6b923a39f8510edae4b1dab690741099c26a2`  
		Last Modified: Fri, 24 Oct 2025 20:37:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:b0ca94d864c544a5e03540a60a792666cc869dd98497ba4640a9035c47f26212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7dfb3a4764bbc729c9469d15809853a7e1010b689dd4bb3e01467d4e46cacf`

```dockerfile
```

-	Layers:
	-	`sha256:59ab2fc40e845bc5cbedad011d2dea2cb0c7f2a0b275a318bfd1ea9964308359`  
		Last Modified: Fri, 24 Oct 2025 22:47:25 GMT  
		Size: 4.0 MB (4001594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e55e5b78e4813c91fdfd416652196bb5350537f0c767e30e0ffd2b6dca552c3c`  
		Last Modified: Fri, 24 Oct 2025 22:47:26 GMT  
		Size: 19.4 KB (19427 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:abcea30560901909b1df07bf4d2ff4c5e9120546932efd1a4dfccda8f64ed965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61931575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90db01e6d7d047be8e63b7ea0afc955ce57882d75ea934567a895b589eb3d9d6`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/perl
# Fri, 24 Oct 2025 07:13:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.4.tar.gz -o perl-5.43.4.tar.gz     && echo '75676cc02c1d4d6f4577f7fd953e07ab5d06f71cf4201753ab6e2b0ddb5a4931 *perl-5.43.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.4.tar.gz -C /usr/src/perl     && rm perl-5.43.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/app
# Fri, 24 Oct 2025 07:13:41 GMT
CMD ["perl5.43.4" "-de0"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c557c959a98283bc362d20d134e6dc168834edd97c55cab266afb4fcb57c8225`  
		Last Modified: Fri, 24 Oct 2025 19:43:18 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076110e14f256f67defdd64788cbd4349a0d77756a11e4dee2774347478a0d8c`  
		Last Modified: Fri, 24 Oct 2025 19:43:20 GMT  
		Size: 31.8 MB (31789182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfa618487487709b1e1a06f483dcc340afdbb569da85258ee07fb479fa1f0b3`  
		Last Modified: Fri, 24 Oct 2025 19:43:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:8ad1fdd38cf6f4e6600301b22975d1ad3acaf7168d0bbfa317c75cacc46d6ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748660ead77af03b38e00b0613cbccbe41e623cf091570a517747b2144789393`

```dockerfile
```

-	Layers:
	-	`sha256:507556a4d618d2f2647b52d3b2f8f3953b10b7442972492780591e3411cf7fd9`  
		Last Modified: Fri, 24 Oct 2025 22:47:31 GMT  
		Size: 4.0 MB (4004453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a8b99e8fe21a6c831c972a658ea30b2a1cc1218b725746a31c0c4a229ff467`  
		Last Modified: Fri, 24 Oct 2025 22:47:31 GMT  
		Size: 19.5 KB (19459 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:41f306c5f5786eef42161dad0f52887a25fec21c10f7f2a57f3494eaa649974e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66505157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef3d0e1f1588c51f293f5df476666cb13e66811224daf282762354b6668d941`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/perl
# Fri, 24 Oct 2025 07:13:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.4.tar.gz -o perl-5.43.4.tar.gz     && echo '75676cc02c1d4d6f4577f7fd953e07ab5d06f71cf4201753ab6e2b0ddb5a4931 *perl-5.43.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.4.tar.gz -C /usr/src/perl     && rm perl-5.43.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/app
# Fri, 24 Oct 2025 07:13:41 GMT
CMD ["perl5.43.4" "-de0"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db7129308cd5ca6ff9876254eeef391297240738d01aef707ec2d963f4154bf`  
		Last Modified: Tue, 21 Oct 2025 08:32:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb89dfef40cd413031a75bdf408faa7d4eea4a61c03b4302728f5853553939d8`  
		Last Modified: Sat, 25 Oct 2025 01:29:52 GMT  
		Size: 32.9 MB (32906372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49c912ad0b2d7a5bfa2bfc085449309c0e6aaa09747001aa73be53010f675f5`  
		Last Modified: Sat, 25 Oct 2025 01:29:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:932c372037c2d7b6e3d33edf7789b44797890d8ea3109ab21bc2ae63940f902c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f945ced9c86dde145f0d296e37bf2b5446911d4018f87d4e9c2ceb71e0abcb17`

```dockerfile
```

-	Layers:
	-	`sha256:33034cdb30147d5750db46a1423eed844171498cbcc9631e427e66d14f237a69`  
		Last Modified: Sat, 25 Oct 2025 04:39:46 GMT  
		Size: 4.0 MB (4005370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54984f667c519c4bf0ca31d8d828cd38f9b83f770659c3c6efd8c1a661988d19`  
		Last Modified: Sat, 25 Oct 2025 04:39:46 GMT  
		Size: 19.4 KB (19387 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; riscv64

```console
$ docker pull perl@sha256:0b23b9d763075d9c866ae4b6c712aede231c00e16d737f6088991964bba7b807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68106556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891eb284ce0b81fc62fca603f4ae795da0dbf619308b85c73388e8ccf68decdb`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Sun, 24 Aug 2025 06:40:17 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0e6a6abd3768739c5cc84a0210c76a03bfb86afcc4905f9082ae54678f7d3c`  
		Last Modified: Wed, 22 Oct 2025 19:32:45 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d79933d96fe3c7b750b36587bee54f896c01fff0889c5ae8538e5c3bd11535`  
		Last Modified: Thu, 23 Oct 2025 04:06:23 GMT  
		Size: 39.8 MB (39830638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff43c6067a1fc294fb2152b67298dee0cc435de51d46792f0d4ab095e9ad31b`  
		Last Modified: Thu, 23 Oct 2025 04:06:20 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:0e2e0c3dcb75933cd714915518132076e3557fd72152a5e9407086147135407e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34484622a7aa835f5fe5a1e40bb34d0cee6b74036fb43c19956941d1f120949`

```dockerfile
```

-	Layers:
	-	`sha256:ef5d613363bbccaca000a5cd2b3ee14cf3a1beb5ecc07a5e74b10b1d5f434c27`  
		Last Modified: Thu, 23 Oct 2025 04:39:58 GMT  
		Size: 4.0 MB (3996636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ceb5cd473309c0c48f8bf61f0161e0c26702812cf2e80c2900a08db8bc2da3`  
		Last Modified: Thu, 23 Oct 2025 04:39:58 GMT  
		Size: 19.4 KB (19381 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded` - linux; s390x

```console
$ docker pull perl@sha256:8d4162c355a0ddde92482ecfdba5cfe229559de0caf48f0550a86f773a56485b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61335031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4eae54b980b87a3108383d37540aeefca8b61a7120e6714ec1be6013f56b4f`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/perl
# Fri, 24 Oct 2025 07:13:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.4.tar.gz -o perl-5.43.4.tar.gz     && echo '75676cc02c1d4d6f4577f7fd953e07ab5d06f71cf4201753ab6e2b0ddb5a4931 *perl-5.43.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.4.tar.gz -C /usr/src/perl     && rm perl-5.43.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/app
# Fri, 24 Oct 2025 07:13:41 GMT
CMD ["perl5.43.4" "-de0"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731d7280efdc1c0b18b921937367f0e4f8cb53a1805763bc8ef06c861494bfa9`  
		Last Modified: Tue, 21 Oct 2025 14:38:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21916f1bc2710b8b203df248e12a4758ee415bebfbfd9035b4243362ec5dff96`  
		Last Modified: Sat, 25 Oct 2025 05:43:30 GMT  
		Size: 31.5 MB (31497509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432369746c353e63e0dca1f0b87bed8598bc470817684d9dd26a9f8c84bce602`  
		Last Modified: Sat, 25 Oct 2025 05:43:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:0a18be94298df5c4e66faa7173ebcd50cd167e3592fd0917e885dd6da6255675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72b466c6787e418f09c189d13b5fe50ea82fe78f365a63889df3f109016482a`

```dockerfile
```

-	Layers:
	-	`sha256:ec6697290228cc9103dad9c3b3b3a51246293ab5a9b6c3afa5af3ae2488687db`  
		Last Modified: Sat, 25 Oct 2025 07:39:40 GMT  
		Size: 4.0 MB (4001686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fe2820589192baecabb8f063167e65cabcb276b35357cff0ae472848a57a28`  
		Last Modified: Sat, 25 Oct 2025 07:39:41 GMT  
		Size: 19.3 KB (19331 bytes)  
		MIME: application/vnd.in-toto+json
