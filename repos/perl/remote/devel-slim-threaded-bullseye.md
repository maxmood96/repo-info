## `perl:devel-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:1c9bccf0b0d544ddf630dc5ee3bbe0d6a6d2118e7adc421b1c917ec8bf21ae31
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
$ docker pull perl@sha256:001d915f2060abcdbb1dc555b001a6b1f6c6662b94b001011690fc3cc92c5552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57605829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fd1614f9cd8c73226390ad6a2d0f5044ea5e8af652c57dce3134432b20b7f0`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fde6793e75366ea34ecedec3f3dbd299258c9df2e495f0db54d8812e2cb24f4`  
		Last Modified: Mon, 09 Sep 2024 19:20:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07b763c0f775485c50d8fcba87c1b5ece44ac1090f4ce37b30a2fea6dc7a3d9`  
		Last Modified: Mon, 09 Sep 2024 19:20:45 GMT  
		Size: 26.2 MB (26176886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d4da1e97f521a6eac7944c4f2383f7fec7bbcb6ecd4a43d8e67fdd5fb4f5e6`  
		Last Modified: Mon, 09 Sep 2024 19:20:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f939b3a61ed0df91d2cad9ddc147ac70942cf9c2f979fbcae2d7c211f23a02c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df04c456ce8b11091f80e9ac8c2b47d00de13a5c347ad92a25d8ebb2b34c29db`

```dockerfile
```

-	Layers:
	-	`sha256:8e1709390ffe9c0f4685ba96604e2705347b8b799105f0fe465cf74095822d0d`  
		Last Modified: Mon, 09 Sep 2024 19:20:45 GMT  
		Size: 4.0 MB (3989462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c887a6de8067629db4eec62975a7855440538b05c89acb886982415988758adc`  
		Last Modified: Mon, 09 Sep 2024 19:20:44 GMT  
		Size: 18.2 KB (18155 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:a1cdc630da1ec860a1a30be8309f3d39439cd79407ac7b8ed2335baf37686d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49986922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b154f73b65f3cd9519f9e8cb53e71ca915751e8885935e3099372179d82eb81`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:29 GMT
ADD file:c451ece1244c14bce110ffbe6906867ce12f8e88234988b0edba91009a9dbbf8 in / 
# Wed, 04 Sep 2024 21:58:30 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:f572303598915f7fb61cc4b47f7207c9ee64d52b9db5fc03ee133ec2dd679347`  
		Last Modified: Wed, 04 Sep 2024 22:02:25 GMT  
		Size: 26.6 MB (26589615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53185675d6d94d789791a2a9c8524d19b7bd6c3dc0fd5c303e79392043b9051a`  
		Last Modified: Thu, 05 Sep 2024 04:59:42 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f8c3c5906e5d55f3a784e1ea1ecff36e1398437b50005b198fba159e52628e`  
		Last Modified: Tue, 10 Sep 2024 04:46:23 GMT  
		Size: 23.4 MB (23397043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0e266a55ebd0e469fd95ecd1fb44b58c9287d51385f79b4c343ed74e0e52ee`  
		Last Modified: Tue, 10 Sep 2024 04:46:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:618f027626d70454061d92d645c8129dff8404a0ff644d42d75b2651a9989e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3981630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3f13ac453cc9ff0928c533c4d40f8cb08180ca10698436e3d76c665be569fb`

```dockerfile
```

-	Layers:
	-	`sha256:f77bae36aab6ed72d0495159afa75ccec01494cf54a8cc24c3063f2c5bac633d`  
		Last Modified: Tue, 10 Sep 2024 04:46:23 GMT  
		Size: 4.0 MB (3963413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ce19bc493061d78db976f38bbbd0663953d861bc09ef290b591ce5bcfe7c28`  
		Last Modified: Tue, 10 Sep 2024 04:46:22 GMT  
		Size: 18.2 KB (18217 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:80a8e6663a59c467703ed6ef446689ed2d40a13a9985bbf9da8e00ebad66081b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55357263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fed799a8337fe5cd3c22902b3fb8517a3d4be7dfc6355e77f1adce6ef54dae9`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c58ea52dadd28d28e72e1bbe20ba15e2b5ed001835816296088c95200a3d1e`  
		Last Modified: Mon, 09 Sep 2024 23:34:05 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e352c1be169e061906373a7dcfaa5a4fc3f3b8d110a2f01fef0465d77240efb`  
		Last Modified: Tue, 10 Sep 2024 06:34:15 GMT  
		Size: 25.3 MB (25282632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d89305a9edb360e7aabc5e230feb9190a9535e40cf6c70d01d6658c2e6f795`  
		Last Modified: Tue, 10 Sep 2024 06:34:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6a7cda40fdcd54af04be04bde6a403a464eb3e2fb6f0567fdcbee78616fbdcc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3982275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93a2d2401bd28c6fc2653c69a8c6f5cb904db32be9d93dad22e3a304a428e89`

```dockerfile
```

-	Layers:
	-	`sha256:5381b8deaa01e94db333a49e28b9e6a58aafbd18375595c5bc36e798806fcdd7`  
		Last Modified: Tue, 10 Sep 2024 06:34:15 GMT  
		Size: 4.0 MB (3963823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63042d1512090b411438fc5f824d64ae052b6578f3be92f391b7f0524785f66d`  
		Last Modified: Tue, 10 Sep 2024 06:34:14 GMT  
		Size: 18.5 KB (18452 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:0dfea397c3c441ae93e267068e305c7e4aa64ca520aa1fb0a05c1cb4a76f3699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60145000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2eae26b007cb4c7dda693c9206109034e599e89d41dfacdb530c609768479a`
-	Default Command: `["perl5.41.3","-de0"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:56 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Wed, 04 Sep 2024 22:44:56 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.3.tar.gz -o perl-5.41.3.tar.gz     && echo '7b9cd0f84a5350ea485ae6c57f3231d338f8a00c23f193db3964a60d38cf8850 *perl-5.41.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.3.tar.gz -C /usr/src/perl     && rm perl-5.41.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.41.3" "-de0"]
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e79ee89fb4fc410ec0c465461d34b972e2ee4a94b25b1e16636f69fc4ef8cc`  
		Last Modified: Mon, 09 Sep 2024 19:21:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0228874fcd1baddd792a6e0696b8c1059383e148e5d2c07a04299627297dfdd5`  
		Last Modified: Mon, 09 Sep 2024 19:21:16 GMT  
		Size: 27.7 MB (27731421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6450e8b8e982de5ceed62509d009c3fe8074a2b96eb47ece73f1d77b50b02b51`  
		Last Modified: Mon, 09 Sep 2024 19:21:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b1e26e709834cf8871642258d448156a755c9b5e062d74f3a7b8a3c141562272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4011821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39ed629691f8c02e64b647cc12c19ea20b940089b445e270936422ae7ebe216`

```dockerfile
```

-	Layers:
	-	`sha256:9212d2ee72c05905f2431039099b02e0df20659dad7dc7a0271d7fcf913dc3e4`  
		Last Modified: Mon, 09 Sep 2024 19:21:15 GMT  
		Size: 4.0 MB (3993690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d09f52a8efbabaad33dc7b93ce34f2d69082cc9af9979482ceabca96b0326be`  
		Last Modified: Mon, 09 Sep 2024 19:21:15 GMT  
		Size: 18.1 KB (18131 bytes)  
		MIME: application/vnd.in-toto+json
