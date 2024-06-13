## `perl:slim-buster`

```console
$ docker pull perl@sha256:cf43ce0d0b8023e1435c8b11acd467268dba564ef68ed3ab525f3a4341a681e8
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

### `perl:slim-buster` - linux; amd64

```console
$ docker pull perl@sha256:e32fb51607d5224989f176c5e6c8e513980f8b366d3ac8bf9dc5a07c1c44237b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54967729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79038f58858bc00911214b72480a9b700678bdddd5dd7a240c048b63dcf3f99c`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:28:45 GMT
ADD file:ea1fe4f19165d885a1f3d523e0ebdcc3e863e6b93717c8022529edb674a52e2d in / 
# Tue, 14 May 2024 01:28:46 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:6299ae3fea5d052b297d91a57200563362b8f2c95358c6e3010d6fa3ed44e7c4`  
		Last Modified: Tue, 14 May 2024 01:33:45 GMT  
		Size: 27.3 MB (27337664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afa17c61e296ae8684dc124d22b6e953cc8102d0958c0d5459e53f5966c622f`  
		Last Modified: Mon, 10 Jun 2024 21:02:43 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b49db520b6dfc036995b7fb08eea7341d51a5e32e6b144af68bfc457c09d83`  
		Last Modified: Mon, 10 Jun 2024 21:02:43 GMT  
		Size: 27.6 MB (27629797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd60c6d1678ff60062cc10b2d31df08c314b65978bae435af88027a08fc12226`  
		Last Modified: Mon, 10 Jun 2024 21:02:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:274cca9b036ae9c1a811b6de439c2f04124e907534f581970f039e19836d3daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d59257eeea3cbb34754fd3f1f61e06e89202f08b40b1a6835bf238d30d0302d`

```dockerfile
```

-	Layers:
	-	`sha256:5e904041807c699910ad1deac6136f91284942e04edffff2fbd91ad4ee4e14c7`  
		Last Modified: Mon, 10 Jun 2024 21:02:43 GMT  
		Size: 3.7 MB (3721513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea381231d71176069e25aa8e94fa45996ffc29aae15a42126614dff471bb0f16`  
		Last Modified: Mon, 10 Jun 2024 21:02:43 GMT  
		Size: 16.2 KB (16220 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:07938d1db587370bcae96bc37a603990fe41145ae12a07128d3b3d336cc22d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47153187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c59b0ba133c37c2997c1a6441b7aba97dfc36f54def2e1af1791afdb3a94d42`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:09:18 GMT
ADD file:e48e4c164cd443d649cca91f392a3ddadac422905ad4f48aca0f47eb2243561e in / 
# Tue, 14 May 2024 01:09:19 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:30a8958fe0d5b6c3e6d6c11772c14c4b85029786ca86968f09e078645df26b2c`  
		Last Modified: Tue, 14 May 2024 01:14:02 GMT  
		Size: 22.9 MB (22944934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25a99f46ff124a1f0b32543fed81f02fb157235f368ebd139dad111d286efec`  
		Last Modified: Mon, 10 Jun 2024 21:35:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cae4f54760b69677de3fecd9dafc53c212133d1551c08518109c015cd14adb`  
		Last Modified: Mon, 10 Jun 2024 21:35:54 GMT  
		Size: 24.2 MB (24207985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb19644a93acf4eb35d4ff0849d113a47855973a46d0b4f6ca6a338790048eb4`  
		Last Modified: Mon, 10 Jun 2024 21:35:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:cc92d512701a7318123b3c35eeb76acd02b8f8b7e3684e6f05c521aee9ae45a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac54c17215bb51bcd5d2c09031e7874b1c0cf331a1cba51ed13da84587fd05b`

```dockerfile
```

-	Layers:
	-	`sha256:d322efd94bc84db89ec041c1859b673b0cf4206385fad28ac04c49026a8f1de2`  
		Last Modified: Mon, 10 Jun 2024 21:35:54 GMT  
		Size: 3.7 MB (3696731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5e2412d8ffceac0d36d87b2602b389f77e1a0179e4582bebbfbf9d69447447`  
		Last Modified: Mon, 10 Jun 2024 21:35:53 GMT  
		Size: 16.3 KB (16300 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:b02b8977fa4586e8fe3040d6009e4b198a207c4ea9cee4f4fcad243dd572afd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52373492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4521afceb4a3103d35e5c9996733622344711837814d6409c0a1e75ba9daadf`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:ad8110ff35cfa20fc3638a9f2a63a1113c1e4f724bc3b8c11d7ae280154356ca`  
		Last Modified: Tue, 14 May 2024 00:44:04 GMT  
		Size: 26.1 MB (26109106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a65d71fe613819c7476b2e0ef7cbe951a8f1dd109d9fccc10c060567787c31`  
		Last Modified: Mon, 10 Jun 2024 21:46:19 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bad89dfe32c6565ef93c23127afe1d4b58ce8caaa893c609efe81f8dffc59d`  
		Last Modified: Mon, 10 Jun 2024 21:46:20 GMT  
		Size: 26.3 MB (26264118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65e8598a33f4a0a2df5baf2342f129fc4c259cb1dcb96f57e579bd5fc339584`  
		Last Modified: Mon, 10 Jun 2024 21:46:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:175ddefab2661aaec6f8d94aed5311541d7474066ba69d9e77207716a885d9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ccc39da02c2bcd870e6dd45ae48759fb2f798c00d20db9d673120708202f713`

```dockerfile
```

-	Layers:
	-	`sha256:0cdfecc0132393df81c5e82bfe14b74804892b16345b8aa846a4493cfab1e0eb`  
		Last Modified: Mon, 10 Jun 2024 21:46:20 GMT  
		Size: 3.7 MB (3691040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2b4c89bf593e3c7f7837ff12ef8ee77505bc80b229b335c5d7476cd2ce85c43`  
		Last Modified: Mon, 10 Jun 2024 21:46:19 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-buster` - linux; 386

```console
$ docker pull perl@sha256:0dccc0a8d351017ce09c716efd8ec2979c94a778efbeda26e760d8228b98b8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59755277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941ead62cadb4e598352800c6b665040da19ac44a553856e017bfcd3f78561e1`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
```

-	Layers:
	-	`sha256:1dfc643447ff7a82c599b429eda0d998c6dbad4ab2786eed580821b5b888204e`  
		Last Modified: Thu, 13 Jun 2024 00:44:44 GMT  
		Size: 28.0 MB (27994640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1d343c9066849c940931daf49aac8a64ac58cde9e2dad40fce7fd2a5e2e1e7`  
		Last Modified: Thu, 13 Jun 2024 02:12:21 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130c80f9df9d8406afc306000f733642f049c0da4dabf339ed786bfadbdb0c3a`  
		Last Modified: Thu, 13 Jun 2024 02:12:22 GMT  
		Size: 31.8 MB (31760370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403add8f1b305aa081223d74416a1f10888cc759530427f24d53f1a88d925ff6`  
		Last Modified: Thu, 13 Jun 2024 02:12:21 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-buster` - unknown; unknown

```console
$ docker pull perl@sha256:970fa0b537baa33922129b1935b7b5c7246f057bf2dce7e0dd3eb51bd4cabfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041822f7f571ee9e8a3b2df414ed71fd7c1e58af193d42c15151f5dedab0d867`

```dockerfile
```

-	Layers:
	-	`sha256:83a2bec33b92364f1ba0ea560f4a01a6e3853b16eb553f8b0f4617d4036285e2`  
		Last Modified: Thu, 13 Jun 2024 02:12:22 GMT  
		Size: 3.7 MB (3740310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:741c563b18f9f4912450fb8995101921345f608beb961df261f1b6989bda48d6`  
		Last Modified: Thu, 13 Jun 2024 02:12:21 GMT  
		Size: 16.2 KB (16187 bytes)  
		MIME: application/vnd.in-toto+json
