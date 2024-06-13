## `perl:stable-slim-threaded-buster`

```console
$ docker pull perl@sha256:91b9fa5f53d9811ff122ea78684dfeba26b1a2aef5c47eb0b9ed9180108f6221
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

### `perl:stable-slim-threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:248cdc667932742c9a84ebb7996fdb73b03e8d226c490a760387b4de4618ebd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55024891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b82bd86dfee975b4a18eff69cd4456295e7c6ae9917593b103797f98b5416cd`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:28:45 GMT
ADD file:ea1fe4f19165d885a1f3d523e0ebdcc3e863e6b93717c8022529edb674a52e2d in / 
# Tue, 14 May 2024 01:28:46 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:beb446f359498d4e7b7c82fbde13a63f35ce73d6f51c68dea2d5347e7397f79c`  
		Last Modified: Mon, 10 Jun 2024 21:03:36 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c924e7aaec495d9e473cf25bb21b49f1ecb9fafdafda3400f887d8884a0c84`  
		Last Modified: Mon, 10 Jun 2024 21:04:03 GMT  
		Size: 27.7 MB (27686959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d843449467b29e4ed90c4a37b7803b507afd53f859b7ccb75723508a53cd52f`  
		Last Modified: Mon, 10 Jun 2024 21:04:02 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:486b130083c5a4efbd161ef157c2a529e18396b1e53ccb045eed7776d2d13bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6497391230d9e926722f4eed695fafb9c0f450ee64627cd4afd13ef6ab736e`

```dockerfile
```

-	Layers:
	-	`sha256:d0fe20b6795dcc2cf4b0eaaa01521e4298921aaace0fa613d0bad9b2836c58ab`  
		Last Modified: Mon, 10 Jun 2024 21:04:02 GMT  
		Size: 3.7 MB (3721603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:711e0b300c81492873c9bb39af44092e318042e8f6215f5bc3e50a73d1f67f0c`  
		Last Modified: Mon, 10 Jun 2024 21:04:03 GMT  
		Size: 16.4 KB (16359 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:3645883d8f117ea6f5e13d2fc5665028eae8c71375c5608a264e148a51bc5366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47176896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c719072f2f506ddd3c1f6770bfb6bdcf433da4464b1dfbaf9e338afa853e060e`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:09:18 GMT
ADD file:e48e4c164cd443d649cca91f392a3ddadac422905ad4f48aca0f47eb2243561e in / 
# Tue, 14 May 2024 01:09:19 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:6489dad1474984156456d090b2db7cff9baa25940bfdfc601ccb25e7973ea989`  
		Last Modified: Mon, 10 Jun 2024 22:18:41 GMT  
		Size: 24.2 MB (24231693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9082bb2240260c02eac1a3d1533ffa1e6d5cc84c9a918542693ee7bf7aed149f`  
		Last Modified: Mon, 10 Jun 2024 22:18:40 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:d07b4a10dffe3588be2d160f03cbff5797b9b67959302a62b1b554e3e3f241dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b147a9e243889da2a159d728cb0fffebcc2434b7afc5d9bbaaafa60e6caada`

```dockerfile
```

-	Layers:
	-	`sha256:a1fb3c07b8e4dccbf51ab70fb694e2d871eae1161e113cae4b2572a792a82949`  
		Last Modified: Mon, 10 Jun 2024 22:18:40 GMT  
		Size: 3.7 MB (3696821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:414d357ca52f03b306d433dc28c015f1c349f8e58b05494d0e883d7370432001`  
		Last Modified: Mon, 10 Jun 2024 22:18:40 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:62e4f50710e2c6d506dfcb517c0f27e0797cba2921ca0dea170b198ab9759cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52406970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea848e5178cdadb2b05650d03a0a9da8a25135e268e766979448440099bed27`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:40:08 GMT
ADD file:469a091f7763af8b8b723185853358a0516954941c82654915e259a2356612ae in / 
# Tue, 14 May 2024 00:40:08 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:0911b001edaf59eebe2dbc6aaca36978df5f4fdd6c195cdbf842bb9f707ac52a`  
		Last Modified: Mon, 10 Jun 2024 22:33:02 GMT  
		Size: 26.3 MB (26297595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922129a905215dbbb27112b9ca1532ab6b7773710adb66a9b139cffaeac5862e`  
		Last Modified: Mon, 10 Jun 2024 22:33:01 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:30dca232208f3b036378cc081c7a1f0d2c1fb6fa8c36bada11759b9dd0b84e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9d35f22d55cb6797980a8922e78492d285ec0da5c6ed3338d3b89116abfb45`

```dockerfile
```

-	Layers:
	-	`sha256:8ea0482369504bf326d179e53caf2cafdec24c736f0e2c21426544f4a27b546e`  
		Last Modified: Mon, 10 Jun 2024 22:33:01 GMT  
		Size: 3.7 MB (3691130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436427df5d29ca1f03587c7cd894421f91fc5fb7c6929ba3be160b1ec783ac73`  
		Last Modified: Mon, 10 Jun 2024 22:33:01 GMT  
		Size: 16.7 KB (16678 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:301d560afedcf75bd0ae8254708d76b7aceaf60f4b6b24b038f73e73fba7e248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5834248c46b06d73cbc18d51c9f93d99dc2daa5736b835967571fc51077b2b1d`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Mon, 10 Jun 2024 03:33:39 GMT
ADD file:7bc8fc617f718bf5e65e7fd718531a01122acc1783af5233c98aa9d31b0f093e in / 
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:8e8408cd07aea0835599bd193bebc8e93fd487049cec2a46ac848b1018a19944`  
		Last Modified: Thu, 13 Jun 2024 02:14:09 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0e3cca8180cac0fdeecff8fe38dd947213943bf4402284ee0cf4b8884dff4c`  
		Last Modified: Thu, 13 Jun 2024 02:14:11 GMT  
		Size: 31.9 MB (31858254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303ae87e2cf1e53d645fbdef9bb6a57a808bc44a22fdc6ddccf8001c01b27586`  
		Last Modified: Thu, 13 Jun 2024 02:14:09 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-slim-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:b9dd495161aef139e1c5ae66a7b43df010df197cccb1d3c2e25e3cd6958a43e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732dd2790712eed22d35ca5a85e43680381bf9b7f9c013e9da9789ceca76bead`

```dockerfile
```

-	Layers:
	-	`sha256:9ca77bd462302ed56df92e999b8b1a170aa8e35692e4913030e6508e3b5f035f`  
		Last Modified: Thu, 13 Jun 2024 02:14:10 GMT  
		Size: 3.7 MB (3740400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8180f930840390375ec866ca4f16b6f91682f68b38a589a54bbfb77d3eb8cca`  
		Last Modified: Thu, 13 Jun 2024 02:14:09 GMT  
		Size: 16.3 KB (16325 bytes)  
		MIME: application/vnd.in-toto+json
