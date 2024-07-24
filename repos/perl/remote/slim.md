## `perl:slim`

```console
$ docker pull perl@sha256:75780588e4d5edff6c9bea07379f72d09a441eefc7e685b48f8be39d702b8a55
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

### `perl:slim` - linux; amd64

```console
$ docker pull perl@sha256:4ea49cfa0f16419d2e42e59cd8e17fa26a2fd682fc0eebcecf24d429a569ede1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57791469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547aa2d1c577cbeab0cf7b9b323534de6400aef2c46037bd21d4e193e1eec122`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a75dbf0068c71a6a16c94213428a2d78dbe82faaacf58fd06aa44ab0f10ac1`  
		Last Modified: Tue, 23 Jul 2024 07:27:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1a492ee3d955a7afb21a47b9b274a550f0ab1d7e58fc02e1ead3b7f9dddc7e`  
		Last Modified: Tue, 23 Jul 2024 07:28:01 GMT  
		Size: 28.7 MB (28664915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd34f8ae9cc96a361215dea2d555b95cbf154ca080edef5484c750c0de4478d0`  
		Last Modified: Tue, 23 Jul 2024 07:27:59 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:25847a97887cf046e2b271ea3cf7a1652e1a069c2e9ff20a5bfa237873edf93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3762136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52f3f970e77b2a803e697aa68d5dd6bc8b29c8fca4171b5417c1961d829f0e0`

```dockerfile
```

-	Layers:
	-	`sha256:d5fef73cc6b377e188b3094a1b388df2f5a11a33c35ac11fce517079052cd956`  
		Last Modified: Tue, 23 Jul 2024 07:28:00 GMT  
		Size: 3.7 MB (3742732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb9426fe0f7ec2aa206f488233a4b13089ceb8be0d3c619b2e24c51d08557d9`  
		Last Modified: Tue, 23 Jul 2024 07:27:59 GMT  
		Size: 19.4 KB (19404 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; arm variant v5

```console
$ docker pull perl@sha256:ae0fddbfae06ec2ba6b7ea89f1b55c8b7ccba403acf261ec8e6ab3a932429905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52661370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a9a126112cefd20e3a2ba7e86e35610ba8a362760428772b67b0ec3e514ac2`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285f79bbc1df7e0d943cf06d95562c4e28b718ee9e34c116b9be23f5b5478b68`  
		Last Modified: Tue, 23 Jul 2024 08:24:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1445ff7dc3658942d68dcd85e0258bf65a71c3390dda932eb89754cd6dee04`  
		Last Modified: Tue, 23 Jul 2024 08:24:19 GMT  
		Size: 25.8 MB (25773804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc18749c12c16d7ea1f67306c13ba9eaba733b009c0d622d04fa829c8e217b5`  
		Last Modified: Tue, 23 Jul 2024 08:24:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:f4a2be38f97230c6c9456cf038da7ea22735e3b2922b7671d54379f273468dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79de661539fc8d59a0aab7f75ef1131791db89fa8c1cb70eef952b1f8608ec83`

```dockerfile
```

-	Layers:
	-	`sha256:66bf9363d3b649b62f26c1d100ca742834fdfd7c512a64ed319a029a49a69268`  
		Last Modified: Tue, 23 Jul 2024 08:24:18 GMT  
		Size: 3.7 MB (3713170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5efb308a8ec1341427735fe85c5838cf229a840405812b2d2b697017913c36c8`  
		Last Modified: Tue, 23 Jul 2024 08:24:18 GMT  
		Size: 19.5 KB (19522 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; arm variant v7

```console
$ docker pull perl@sha256:c9a724c929c1ddfeaa097257c7f536f2a8df2db4fa4d37ca9202d894f29d33df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49704120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674ab616270b88d215fd6ee4c7eff545a92b0a7cd4ed6e6b3fc8abc5630fecf5`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4feb632771abbe21f4e6a0135dc4434d1753290265a4e55b492593837e1ff0`  
		Last Modified: Tue, 23 Jul 2024 23:42:29 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe02acebd7ed95937ef077760ebdd95145df6a078d13b370eff1a8ad78b3f31`  
		Last Modified: Tue, 23 Jul 2024 23:42:31 GMT  
		Size: 25.0 MB (24985652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7520cecfd26c7459fabb8b69349e9849d9008bbdfec0799f81393f43b4b03aa`  
		Last Modified: Tue, 23 Jul 2024 23:42:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:6b23d26c6f04ec6287e14cbec754038694a273f49bf6e0b09f9a028f04f1d394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6145cd5ab6157d32a46de53d80487d9977cf60950bfcf92b62658a8868c52f`

```dockerfile
```

-	Layers:
	-	`sha256:b34ebb83caebb9e79a232cb6a784369d047e43bc01168052c0a83a118662c03a`  
		Last Modified: Tue, 23 Jul 2024 23:42:30 GMT  
		Size: 3.7 MB (3712785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1092f43303bbdafd55a6da0c46f459409c3500d67e1da5f9689c1a606c5683a`  
		Last Modified: Tue, 23 Jul 2024 23:42:30 GMT  
		Size: 19.5 KB (19522 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:3d794b38d18798c385edc1e670c3cdf8bcb38b9d069bdedfc1a19489a3cedc10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56617487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35566f3174aefe74e76073818fea6f7e7d5c26a11aff3e62e24f15219e12620`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d7b1b05c3dfb6c37b5824741ba52dc43a7c12886ba89fbb9a40c4434267b4d`  
		Last Modified: Tue, 23 Jul 2024 22:26:26 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beac1e72b9fa817512b426473542cbac6bcf3addbb269ab72bfbc30b79ac112e`  
		Last Modified: Tue, 23 Jul 2024 22:26:27 GMT  
		Size: 27.5 MB (27460648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e031079697c2fb852519afdc5dfb8e55eb1a04a910629d93370fdcebdc07a070`  
		Last Modified: Tue, 23 Jul 2024 22:26:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:b33dcce6102d878b1ed4492e50c4b89679cf24972260dbc792df1722b2b363e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3e3eb445883e2752c0e6665db86875cc1f2fc17ba7e140a714b4f03e45ddc8`

```dockerfile
```

-	Layers:
	-	`sha256:ab83c5f03f95e17f74cfa6db4b3a00608075ed844b12dfb5dee1c16a9c21af51`  
		Last Modified: Tue, 23 Jul 2024 22:26:26 GMT  
		Size: 3.7 MB (3714003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b766e1cbffc1cb2747e3dceda8ac742f0a4b4684c3626529c980ce00f665d9fd`  
		Last Modified: Tue, 23 Jul 2024 22:26:26 GMT  
		Size: 19.8 KB (19785 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; 386

```console
$ docker pull perl@sha256:05ee707f400c260bbdef268fd8b37933d72c892f0829a17bec9f6355f4fbca0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57813794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49883ba3be0870b57d49a92179b533d9b2621b8ffff7e776400886cc0fd4a04a`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:9b63a9d86a51a3d56d700d09e1152578d700ba4453d852325d8eb9896534f3ba in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:7fa64a47f35cb425a1275bff76c45df3b76d3ff6b07911737090b82e4f221e93`  
		Last Modified: Tue, 23 Jul 2024 03:57:51 GMT  
		Size: 30.1 MB (30144309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80576ad5388bc01dca8b4f11e99b755a26122618d4adcd2700735017fa4194c3`  
		Last Modified: Tue, 23 Jul 2024 06:25:27 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7c0b703d02e60cfcdd9b582663cb86761116d4f9d898851cc5d18794a5cb0b`  
		Last Modified: Tue, 23 Jul 2024 06:25:28 GMT  
		Size: 27.7 MB (27669218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dda1df75ef58c518a4d8d6433216b0cd280e5499305e1e2ebf8d37975d09fc5`  
		Last Modified: Tue, 23 Jul 2024 06:25:27 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:0733bada5a8c299668b381a52e0525bc70251070b3636192634cc54f7bdfaf23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf693b48041a7ab20c49fa0a3f92ba3c11cf9e1cbc6b506faece8c27c1252c8`

```dockerfile
```

-	Layers:
	-	`sha256:a365002c504bf3f4d6325dfe50f5971e3b26ee6bdab098afe6c746f264289982`  
		Last Modified: Tue, 23 Jul 2024 06:25:27 GMT  
		Size: 3.7 MB (3736605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37241284e0c45caaab6ae73e65a70cd94cd637d5d3fd1505b33e5abe6e1b68f3`  
		Last Modified: Tue, 23 Jul 2024 06:25:27 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; mips64le

```console
$ docker pull perl@sha256:0d22584e03c1d7808c414d2b1c6e41a7ced7b876b7ccee624c37e92fc45643d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55947741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cba5165dfbec682411b0fb51448e6b6d36060ec9056e2067409658aa9f4d1e`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:23 GMT
ADD file:9a0f0c8ed27f6f2bb89272036da4d44a63dcaf43fb03528dd2d970fbe64ccc92 in / 
# Tue, 02 Jul 2024 01:18:27 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:cbefe199012545da86e0f461f1964dea0c9bab400e37766ee5f32b967423cf0b`  
		Last Modified: Tue, 02 Jul 2024 01:29:29 GMT  
		Size: 29.1 MB (29124929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e792c930a4e5e614eb99ac7a4a956102877f4875a857b860cdfda61ab934f6`  
		Last Modified: Mon, 22 Jul 2024 21:17:02 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d441054870c16fdc6002c5143bddbceaa21ed770b86552bc594b533bfc7c8b`  
		Last Modified: Mon, 22 Jul 2024 21:17:10 GMT  
		Size: 26.8 MB (26822545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f0e3c326150859d5d396406fceda22d1fc5185d2e02a0a55370dc7e5e3a5b3`  
		Last Modified: Mon, 22 Jul 2024 21:17:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:1aea7732e33118b1b3d73c2baf1ca6a8921e2f1d2cda8235f98554687f80fbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3178c4a59ba2d908ac7074a83c05390f7823a825f60a30d12bf621b7fb0f4901`

```dockerfile
```

-	Layers:
	-	`sha256:6f6c4b41fce1f24455f2da412554fd9c00bd4af9eda20ed0e62857103c1917df`  
		Last Modified: Mon, 22 Jul 2024 21:17:02 GMT  
		Size: 19.3 KB (19296 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; ppc64le

```console
$ docker pull perl@sha256:8941f301f0700e79a81eb4631e043db5a579077c8b9957c3c1e1ab0d06e114bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9039fd621145895ea7b53e88da99b02efe6ab80b60db02b97deb9a6f1afb30`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0cb411c15df4d2ceb091e80225e9184fc322db7d7a6be00850ff7591a08a14`  
		Last Modified: Tue, 23 Jul 2024 20:00:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b53a5721ed3362228621a9f1b076f7d9cbdbe8a378665fb14f190dd1b0ae057`  
		Last Modified: Tue, 23 Jul 2024 20:00:07 GMT  
		Size: 29.2 MB (29224265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afedf3545e7b17c5386cc5d57d22eff478e01df2d9a87fd2bab663f7109f42a`  
		Last Modified: Tue, 23 Jul 2024 20:00:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:76bec0f6b5774ff7bd2fed501308bcd1ae7f2fa9c5f0af7f3c75ff8dd6545cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e13ea6cbabf8c4692eabe3c355708828e3b5091743551876a6750f4919d4f95`

```dockerfile
```

-	Layers:
	-	`sha256:8ce7d72bf75393a9f5f212bad4f530afb1fa6bfd73211cfcc8f3ed0468a4da0e`  
		Last Modified: Tue, 23 Jul 2024 20:00:06 GMT  
		Size: 3.7 MB (3728459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b9ca5252a6d8fa90a936501d80060c80fd2c16d0647dea6c9e92bf6d7b0f78c`  
		Last Modified: Tue, 23 Jul 2024 20:00:06 GMT  
		Size: 19.5 KB (19478 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim` - linux; s390x

```console
$ docker pull perl@sha256:06fd156efd4c223d2ccadfc97915be4afb197dd49e60e66534bebcfcbe318d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54696359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a44016db0c1423e1e43453f872dc76be5d2b2a4e51eafb9d5170f0d15dc2f8`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Sun, 21 Jul 2024 16:02:52 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["bash"]
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/perl
# Sun, 21 Jul 2024 16:02:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 21 Jul 2024 16:02:52 GMT
WORKDIR /usr/src/app
# Sun, 21 Jul 2024 16:02:52 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446d679b2c55a374802c8141ac4996b76f2e7e9e7cfefb0d644778e5eb527d77`  
		Last Modified: Tue, 23 Jul 2024 22:38:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f9746d6ec0a002e4b0c0609e7ffc8a53b2369216b0ef9559668cf9686c9d2`  
		Last Modified: Tue, 23 Jul 2024 22:38:44 GMT  
		Size: 27.2 MB (27205993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35395a42385949fb4817cd5b7d70c63ff192e75bbbf2dd5f85f96bbd176ff720`  
		Last Modified: Tue, 23 Jul 2024 22:38:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim` - unknown; unknown

```console
$ docker pull perl@sha256:34dd21fcdab3e14f8600f8533359218d104258178f4be506cd60420385bca797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18660d1ebf296489caad31bc47b2fd41ba2bbd7457e7fdf4aa17a9fde49effb`

```dockerfile
```

-	Layers:
	-	`sha256:134d9fd4e5da62b3b683fdf1f11cc58066b910bb96011279b61bc72fc114993a`  
		Last Modified: Tue, 23 Jul 2024 22:38:44 GMT  
		Size: 3.7 MB (3731002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a68161f009b9dda935e64debbb170b6c8aec1df953ecba205986ea67a93687b`  
		Last Modified: Tue, 23 Jul 2024 22:38:44 GMT  
		Size: 19.4 KB (19403 bytes)  
		MIME: application/vnd.in-toto+json
