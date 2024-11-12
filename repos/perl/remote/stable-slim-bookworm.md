## `perl:stable-slim-bookworm`

```console
$ docker pull perl@sha256:0158ef9a4987d8159492429637c2810262f22b4ac9ad78387ea09b3e9ff35bb2
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

### `perl:stable-slim-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:901d364c453a464a956a96c05eb85616d4ab9f35af04256e5a08fd4d053a2177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59283347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab0c3cb0d5008496bfc31b56d4b98b20baa4334c4c1ae72e0573757d2b02268`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8774723a4af67b30cec1e31530175a03b4365023c416924fac6c73287ff7a6a2`  
		Last Modified: Tue, 12 Nov 2024 02:47:32 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993b1b97b035e4eff356018a133af9584b8bc0c304d571b640c7c0e34b2b381a`  
		Last Modified: Tue, 12 Nov 2024 02:47:32 GMT  
		Size: 30.2 MB (30155085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914789fbc52e20e772873926412637c330fa53427f5648101e5d69810215043e`  
		Last Modified: Tue, 12 Nov 2024 02:47:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:8db28a66f1720aa8a2be821720b983317c2e7f3bdd7e64d79649be535d1fd3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b30bc7e112d2c5d3f5798bc776988fd88e18f977f5acc1fae60453544d1dce0`

```dockerfile
```

-	Layers:
	-	`sha256:580fda998b211700a28e71b2231baaf799ab9932c4aee2ab2f257a06c2b4f2b1`  
		Last Modified: Tue, 12 Nov 2024 02:47:32 GMT  
		Size: 3.8 MB (3815181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f03902496b2bfdbfede058da31a1f5d4f312b05084bc9fdc4baac73a6d2e1d28`  
		Last Modified: Tue, 12 Nov 2024 02:47:32 GMT  
		Size: 20.3 KB (20305 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:138d9858d8d5f5cfcec9339821dface624f8472c86794136e8644717df5b13e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54081158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7b9939fc8a27a2af36bdeab0ae69a447ffb90e1462fcaebb7be7058eca006`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04209475e978f93a62a76f714523f214b85f644ce8192912158891b495d96f3`  
		Last Modified: Tue, 12 Nov 2024 06:57:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41add5b5622f8ca6b4266b1b5db2a48b1709252d2f68cde74a95168ed2265081`  
		Last Modified: Tue, 12 Nov 2024 06:57:06 GMT  
		Size: 27.2 MB (27190833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07c23f5a731a6b0e9c6545b89b1694277930031c132a1e02e4d6ece1af76c28`  
		Last Modified: Tue, 12 Nov 2024 06:57:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:4c0e8556ff3d061894dbe7ba75cf52b83055d82c0aff5e5ba55f32fa8fe26e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c55f3d119ba04831aa2c296c2c11cf6c3ea084aca69449763371af84e8498c2`

```dockerfile
```

-	Layers:
	-	`sha256:71f98bf7daec5e67a359ae3f2a68e84d41967dff258192ee67937208629560e2`  
		Last Modified: Tue, 12 Nov 2024 06:57:05 GMT  
		Size: 3.8 MB (3785737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:911c5c770be77f4c8dbdf35d576fafe843a9a00a6ab81fd7011b7f3b3fd15764`  
		Last Modified: Tue, 12 Nov 2024 06:57:05 GMT  
		Size: 20.4 KB (20429 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:5e2a82012b20efd1695c49b1e6e7af3f32ee2c5d290155518d0aa10d4d9d9cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50998730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1162e879895419b9035444829f1fa5226c92ffd71f7aeed7ae40d5c4c800a68f`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Fri, 20 Sep 2024 18:57:44 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/perl
# Fri, 20 Sep 2024 18:57:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 20 Sep 2024 18:57:44 GMT
WORKDIR /usr/src/app
# Fri, 20 Sep 2024 18:57:44 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb9475168dc9ca57175b1b4be56751886989d3eb029c21f9fb85f4ed1751650`  
		Last Modified: Thu, 17 Oct 2024 15:06:29 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e231fbb5b3c6d8e767131c9d6b2ac600cb7bcf3718f10170d76b23530f24b2e1`  
		Last Modified: Thu, 17 Oct 2024 15:06:30 GMT  
		Size: 26.3 MB (26280266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cb66e3443451a1accc5a5155cecef7d3ffdde49f2addd452c0deaf508a7e16`  
		Last Modified: Thu, 17 Oct 2024 15:06:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:556060af63cc8bc74aa648e56c9a6c18b0ae234aa3503e2487d0f146aed09640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2224c5d880e07aafc472caa1344303d39727c931fad56def18e7aded53da674c`

```dockerfile
```

-	Layers:
	-	`sha256:e4bd1030a6cfd2e2a1943fa59abf1487d585bf7b3604896b2bacce8023f47cc8`  
		Last Modified: Thu, 17 Oct 2024 15:06:29 GMT  
		Size: 3.8 MB (3769913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5edd32013185c7526d77dbab3a2327bb8499ddb652633c89f7d4a1ef3bf4b2a5`  
		Last Modified: Thu, 17 Oct 2024 15:06:29 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:f9fa958559f0d0df8f456dd4fe3035a8797e3dbaaa8c06f951963a85d9c5040b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58107763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb4bffaddf585855e55f0d6492574346a98ef4f6ce36aabfc95602a0097201d`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a474e9977cf240ace93ebc01846ca62f60168c75c129d1d7dbae608a44537f`  
		Last Modified: Tue, 12 Nov 2024 18:50:29 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0497a2aa27565a6efd76861f10496bfe4cf4cff8f7e857f028b46d7fa4b911f9`  
		Last Modified: Tue, 12 Nov 2024 18:50:31 GMT  
		Size: 29.0 MB (28950140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e053c2fd38eb92c6beaaeb10dc1ad9fd8fe50e1adfd33f2cdc0365d0c59aaf`  
		Last Modified: Tue, 12 Nov 2024 18:50:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:dc97da8b4ce20fc90e3c1789f354fac92b26c74cb823cc386cecf713f080ffc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2720ad2ff7d00d80085c3e779f1c458174845290be5970688abfeba68d7573c`

```dockerfile
```

-	Layers:
	-	`sha256:6be3f92cfd76edd3d38c48979f7caa12c5252924c67e8ffd951fb2f534124eae`  
		Last Modified: Tue, 12 Nov 2024 18:50:30 GMT  
		Size: 3.8 MB (3786464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e475a8c3b7a85ef4e2cd429a9f7c1c662c1016e884f976047bf750bd3cc30d1`  
		Last Modified: Tue, 12 Nov 2024 18:50:29 GMT  
		Size: 20.5 KB (20481 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:a2636c3e4b8172d9a3f6c024d00b6a5e7ff83357c4a350bdfe7caf317bda8c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59396394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fafefd50738dc4083d491d8bf0d594bf7576c7e39b44c8dd02393ff319a02643`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8281ea78d717eb092c72dd268ee2ecc358035ece34a5db0b6aef402a470945f5`  
		Last Modified: Tue, 12 Nov 2024 02:47:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b3a531a4205472d1a3db3bf686160b8b122afac9fb21013fdc1b003f094743`  
		Last Modified: Tue, 12 Nov 2024 02:48:43 GMT  
		Size: 29.3 MB (29250678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b588fce55d46b549fd967aca2af6bb29a2f72344472877ca1d25c823929249be`  
		Last Modified: Tue, 12 Nov 2024 02:48:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:8425d721448f04577fa176440ba2bda7f5ee797194fc6bcc2b648a35834548ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3829264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb77431c51022800bc3c3875ea31da2733b27d6a44ce2ab105d1b96e02a4649`

```dockerfile
```

-	Layers:
	-	`sha256:b48bcf3950b11a02c93fa3513b354a71377e107d771137b6bd9b100632b3deac`  
		Last Modified: Tue, 12 Nov 2024 02:48:43 GMT  
		Size: 3.8 MB (3809021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d851a8cd9e07d515debd9f4033b5a36a349aa48a089df7cdf04720721a0e465`  
		Last Modified: Tue, 12 Nov 2024 02:48:42 GMT  
		Size: 20.2 KB (20243 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:5abbc7aa5417ecd75d146a2fae336917ba4570563ba9e92b04806f5abe6c9389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57413885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272cfd1f175c911bbc613b11da1de00841041636f7de4129775da35a465888c8`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:01c6d0bf10848996e396c89b66742849d41fd852c3610146badf9f612e62945b`  
		Last Modified: Tue, 12 Nov 2024 00:58:28 GMT  
		Size: 29.1 MB (29127365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b89d5e57307ec2f1405db8226a1599ac4a166fd8b65c372ab6fdf09dc056c2`  
		Last Modified: Tue, 12 Nov 2024 19:25:29 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453accb52a47c1ca0d36dada5b8cc31181aa9d164ead67c9126c0bfa448a1ac8`  
		Last Modified: Tue, 12 Nov 2024 19:25:32 GMT  
		Size: 28.3 MB (28286255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be772b10bc56124403aaeeb09d86323aa1bf48eb9d163f4396511cc7d3ecd2fa`  
		Last Modified: Tue, 12 Nov 2024 19:25:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:53e55d3902f8a751735af6351bae70cab219354b06022d73562ac2db76f40862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e4cb701f2934233058256c62a5ed7b67b77b70b28203080ee51e8720ae8d35`

```dockerfile
```

-	Layers:
	-	`sha256:b843583e59df619d0fe980d6202e58b9e616c4337d95172b9d8d66c6b8bd7335`  
		Last Modified: Tue, 12 Nov 2024 19:25:29 GMT  
		Size: 20.2 KB (20208 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:a2ccfa74d22eb0e16f5244bcdd960ed84aeceebd6db07ebab60c424e457fbcef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64043833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5260902daf89c391d3fd40c3ab210cc7c8ccaa778b3463089693f4039cf9b030`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038dec34a00d814cd80151c62bdf80c416dedb23d4e1a4281867789fac6e604f`  
		Last Modified: Tue, 12 Nov 2024 10:20:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141ae3504414b31e3810f86dd73b89c44701969f916303afd03ed39450e954f6`  
		Last Modified: Tue, 12 Nov 2024 10:20:14 GMT  
		Size: 30.9 MB (30918213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088292030fc8bce79a91aa98197fadfe3ac5e3c463b8598183687eb46398441f`  
		Last Modified: Tue, 12 Nov 2024 10:20:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:df0c3147a7a58f49225b947b1991c9300a5db89f03dfd493abc6aceab9dc0fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3821371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddebe9e735027e861f4ee6b84852404e46101f12776f32d5d6cf1b517c50e9bc`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e0465779d3e8c32bb8c530b9442865d44a1a23ad228301d40f3801730c852`  
		Last Modified: Tue, 12 Nov 2024 10:20:13 GMT  
		Size: 3.8 MB (3800986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fd15fa37045643430364c61645ec40659c51908bf7d3fd142cf91d5135e29f0`  
		Last Modified: Tue, 12 Nov 2024 10:20:12 GMT  
		Size: 20.4 KB (20385 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:cba63881b746a0db4cbd99c9e56d6b2e855301991727462794f7f64ae07cc096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56165511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c538fc7b812b81964ff761a88ad751cded5895f4bc93c03e9c39bc1024b0c15b`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 21 Oct 2024 16:04:30 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["bash"]
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/perl
# Mon, 21 Oct 2024 16:04:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 21 Oct 2024 16:04:30 GMT
WORKDIR /usr/src/app
# Mon, 21 Oct 2024 16:04:30 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a6c7dd8a651e2ba69544a46bb623124f069c40425a7a7994d936c7f9ddc447`  
		Last Modified: Tue, 12 Nov 2024 17:42:02 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5930479b5905e4b524eae55ce0865b8de25c5e76d93a48c64b530ea49ac4b205`  
		Last Modified: Tue, 12 Nov 2024 17:42:04 GMT  
		Size: 28.7 MB (28673618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad24e9262c0d51489c3110201154abae7e17a621e11150af29b239bc7d8704e3`  
		Last Modified: Tue, 12 Nov 2024 17:42:02 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:90fe4c0c274fe6b40fd3e363783596b2959f17d2e059cf6a99cbc6a4369a41f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3823638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bb672e4c00b508678e54c71de64a6edeca036e618152f93d83ee901b31f3b6`

```dockerfile
```

-	Layers:
	-	`sha256:2bf91b31dce25ee7f7bc8ec7dc1d2c2b2e77e5025fc4e1ecf780124e4a2fd31a`  
		Last Modified: Tue, 12 Nov 2024 17:42:03 GMT  
		Size: 3.8 MB (3803333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f24f13f8ac214484ebc064ddd2aef7a526c3409a7e411e48cf5806554848f6`  
		Last Modified: Tue, 12 Nov 2024 17:42:03 GMT  
		Size: 20.3 KB (20305 bytes)  
		MIME: application/vnd.in-toto+json
