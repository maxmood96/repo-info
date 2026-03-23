## `perl:devel-slim-trixie`

```console
$ docker pull perl@sha256:4b9ddcd8398c10eff5cf9e47771a7770c9f4b4c6a61dc5c68e74e576403f4f8b
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

### `perl:devel-slim-trixie` - linux; amd64

```console
$ docker pull perl@sha256:fecfc03183ca84caf81b9fd3fdf38ba5d63a1ab852012781d071db72db9a36e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61988714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6385fc7dd4a78c5f199b67d80b1a3b090c2a4751b9951723e118490766aaf2`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 17:12:59 GMT
WORKDIR /usr/src/perl
# Mon, 23 Mar 2026 17:17:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Mar 2026 17:17:32 GMT
WORKDIR /usr/src/app
# Mon, 23 Mar 2026 17:17:32 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0388d41a26ae98b6017359d3c11bf6b7dbaffe1e3cb22be57514033fdfc6c4ea`  
		Last Modified: Mon, 23 Mar 2026 17:17:43 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf8688bb4220b3efaea3106fb17f484a543e8ba1e78646d2b69ac749e8a9d7f`  
		Last Modified: Mon, 23 Mar 2026 17:17:44 GMT  
		Size: 32.2 MB (32212949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f92aa7df958279aa3e8937a79a2f2efdf71c95c3b393f1724f7293c4e5ab6d4`  
		Last Modified: Mon, 23 Mar 2026 17:17:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:cd11a19eb5e50189987a3d648de00c78c99f4f716a3a987c44daab6901413eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f50f895cd15eac30966aaf6d5827f06e30743e6216505802e1a103a42e78a1b`

```dockerfile
```

-	Layers:
	-	`sha256:0386751b197e20f9ffc7cbbc9172ec5a1241a967c1cdd4a57167d6df76dd451f`  
		Last Modified: Mon, 23 Mar 2026 17:17:43 GMT  
		Size: 4.0 MB (4009450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e443a0c1bc7be2b1204d36c863e9ff8c400ef8ce68755778728d2d683756ad00`  
		Last Modified: Mon, 23 Mar 2026 17:17:43 GMT  
		Size: 19.1 KB (19129 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; arm variant v5

```console
$ docker pull perl@sha256:08be99f6be1de70b5e1cbf33bd0487592ee8898623908210faecfab02bf7de42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57410739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed15bc9f57a0c3d81c2bae2c5e8f7095d6885abf8e2d16d8e2dc919d9e2442f9`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 17:34:39 GMT
WORKDIR /usr/src/perl
# Mon, 23 Mar 2026 17:40:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Mar 2026 17:40:45 GMT
WORKDIR /usr/src/app
# Mon, 23 Mar 2026 17:40:45 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ee0f9d93a6b1d116c479fee34279c93e5f46122bc8b0804fe5a17a44d6a746`  
		Last Modified: Mon, 23 Mar 2026 17:40:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d382b1e03b7ba91c50bddcc97b2d79d94b5c6fd0de2be1ef56e76c7f3e455b1`  
		Last Modified: Mon, 23 Mar 2026 17:40:57 GMT  
		Size: 29.5 MB (29466823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3e4811ab0e2df88c592d248a8d3267e80e84de8088072aeb5769da06f6d44e`  
		Last Modified: Mon, 23 Mar 2026 17:40:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:e5ee6b562658158babf87ff495c4949fc8ad894c0be4c6038d70fbef278d5d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f912023e55736f2ccbcec41e9d2afa3ee1535102471e57ab9953427e90c8da`

```dockerfile
```

-	Layers:
	-	`sha256:7bcee7daf992da1a02d09fafa8ed2271ba95120b9ded55956a73874bc94ebbf0`  
		Last Modified: Mon, 23 Mar 2026 17:40:56 GMT  
		Size: 4.0 MB (4002495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cfd170b784439848d0c3ccbf9638b6a6097df204994be20fd5e803ee0384d6b`  
		Last Modified: Mon, 23 Mar 2026 17:40:55 GMT  
		Size: 19.2 KB (19225 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; arm variant v7

```console
$ docker pull perl@sha256:bd65b907a5d24e1685db36bccf1488fd44f856161016c0767565e56a1924b9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54742926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08beaad0bb49a97211499b102a2d054f0f036d6940963ebfc14e45f240779d21`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 17:13:10 GMT
WORKDIR /usr/src/perl
# Mon, 23 Mar 2026 17:18:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Mar 2026 17:18:43 GMT
WORKDIR /usr/src/app
# Mon, 23 Mar 2026 17:18:43 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a43297c0fdf2bae4ca7cb498259750700cc8c80a0e38fb357d9b828e74ea476`  
		Last Modified: Mon, 23 Mar 2026 17:18:02 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0accbfc3f5fadb13c03c854f091f0012a2ffa51435f844823cc1fb286699cf78`  
		Last Modified: Mon, 23 Mar 2026 17:18:54 GMT  
		Size: 28.5 MB (28533156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9876b174c406fae5f7e61a4015b6b3dd00ed359b0989e81a8326ca3cc01f450b`  
		Last Modified: Mon, 23 Mar 2026 17:18:53 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:64edcb167da5c816da79d6289d4e9d1954d9a895973dd3c8f95c14d77cf9b836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21de8061e816814fb5ab659e482f1241dae7726992af1e5d768e758642cae72c`

```dockerfile
```

-	Layers:
	-	`sha256:e0be92fd9a7ceced51435fd2b2070b23012306476308baee2d317a673c722fa2`  
		Last Modified: Mon, 23 Mar 2026 17:18:53 GMT  
		Size: 4.0 MB (4001686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1745b9bd394ea4c4fbe5c78ad6230d8ff3aa3deac08b9f68bc6ff9237f25424c`  
		Last Modified: Mon, 23 Mar 2026 17:18:53 GMT  
		Size: 19.2 KB (19225 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:84c695ba31d572238f3d0ce9abdcf92cd2e946b4310b8a629a2711e96dadf8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62022451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b620d257058f9ed8de7f1039f2ba4ef0be01e0755bb4db6376f2bec391695a`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 17:13:07 GMT
WORKDIR /usr/src/perl
# Mon, 23 Mar 2026 17:17:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Mar 2026 17:17:52 GMT
WORKDIR /usr/src/app
# Mon, 23 Mar 2026 17:17:52 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e50002172312cc8a70f0538785262ba40bebc3cc97923fc9f7eebbb0aeaa55`  
		Last Modified: Mon, 23 Mar 2026 17:18:03 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3444e1e1c2d07dc160ec1c4f85619b682e51d40d9bc5f25994270744533549`  
		Last Modified: Mon, 23 Mar 2026 17:18:04 GMT  
		Size: 31.9 MB (31883768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0121d7e0ad2cee912bf8611978b721c918b7f8a837cadd6328277f5050fec1`  
		Last Modified: Mon, 23 Mar 2026 17:18:03 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:9b202881ec03bf3680b1007f30c420881f7991a3e3fc4e2832620041f36185ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eead296b82c52ef690efeec554c2ff720defa3b5bd3c8d1d04ed189d377bca`

```dockerfile
```

-	Layers:
	-	`sha256:2df471d6bd666e86635a3e7644cfdb6eb515b5ae87a67a1f767615035336761a`  
		Last Modified: Mon, 23 Mar 2026 17:18:03 GMT  
		Size: 4.0 MB (4004545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9010d0988f4319eeebb3f6918e2ecc0fe62d1b1c826238f3a823b997004104`  
		Last Modified: Mon, 23 Mar 2026 17:18:03 GMT  
		Size: 19.3 KB (19255 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; ppc64le

```console
$ docker pull perl@sha256:ba4d978ad93afc92a5187bbfaa23891e51be3b4ea46386aec625db959388e8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66534852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0622060fef0c817317ddd49c03fc7f49564d21f938bd4ffc4427b3ebc459cb`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 17:20:26 GMT
WORKDIR /usr/src/perl
# Mon, 23 Mar 2026 17:28:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Mar 2026 17:28:54 GMT
WORKDIR /usr/src/app
# Mon, 23 Mar 2026 17:28:54 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2452d2bad28c87d304e08687a2c9a70dacf1290c8d1af1721deb848cd750e5`  
		Last Modified: Mon, 23 Mar 2026 17:29:19 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a92c9e3eccb3a272402c7bdc987d17677e69e1f0fdbfa651f9f17d1e03a301`  
		Last Modified: Mon, 23 Mar 2026 17:29:20 GMT  
		Size: 32.9 MB (32941750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6cb0b65f23ef83cd7cded82cbd8cb7c8765a402beb3763f74e67c25cfa278d`  
		Last Modified: Mon, 23 Mar 2026 17:29:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:1dd299d8341fd88aa35dadfc211115bf7200231efaacb3aabcfd9a1e8e4c189d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1b752e57c4b83ca9afedd10acb267d168a93c7a8f35a53c954914efa8b236a`

```dockerfile
```

-	Layers:
	-	`sha256:428242a04b40b6cf9ff6b7ee00ae4c2ebc39ab3683d696e7898bbd516eb023b6`  
		Last Modified: Mon, 23 Mar 2026 17:29:19 GMT  
		Size: 4.0 MB (4005462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c61039b556af469cd00103fe0be92ced88967b20bcbb897ac3505154d52dfb78`  
		Last Modified: Mon, 23 Mar 2026 17:29:19 GMT  
		Size: 19.2 KB (19183 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; riscv64

```console
$ docker pull perl@sha256:1b49d0098445113edff781855bc172138cdad9eedeb4b73617ac7bf0807d8c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68299523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24301b2716449afed6a69f89f8e7f25a04fdb0231c34b1a7a5a974f3cb19f302`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Wed, 18 Mar 2026 05:26:42 GMT
WORKDIR /usr/src/perl
# Wed, 18 Mar 2026 12:44:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 18 Mar 2026 12:44:44 GMT
WORKDIR /usr/src/app
# Wed, 18 Mar 2026 12:44:44 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecaa00ec5b2cb9be7f3f7e512a61ff5d7515452953ff6c246818ab4b4fd4f68`  
		Last Modified: Wed, 18 Mar 2026 06:36:19 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d8361879262e723b85e9db7040929d2979686048c9a6223f03211645897e7b`  
		Last Modified: Wed, 18 Mar 2026 12:47:12 GMT  
		Size: 40.0 MB (40023621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e28b8fcb1a316a9701d7b9424999820f599476adafff36a868cd4d7f9bfa0a`  
		Last Modified: Wed, 18 Mar 2026 12:47:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:60fcb9e130f11732a30c31ff86567b5277ccfe173dbc65929e0547b00fa67447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67449c1fff9e2371087de37addb42223d7e7323b6afea4027c9ffae05bc234d7`

```dockerfile
```

-	Layers:
	-	`sha256:58250602a780688f1af3889133955ae7c693a1b5322358701daefa0108713103`  
		Last Modified: Wed, 18 Mar 2026 12:47:06 GMT  
		Size: 4.0 MB (3996728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e1a106679e62bd374a06c5f559c61d0318a834ca32749f6c860e8cd044f085c`  
		Last Modified: Wed, 18 Mar 2026 12:47:05 GMT  
		Size: 19.2 KB (19184 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-trixie` - linux; s390x

```console
$ docker pull perl@sha256:cebad84acd65b1dcd040e960042c647b2a8521b96205b63dd28677e7876a8dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61405705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0301988680637ccf6763bd36c51d0c3f35755813ca7db87da66306d072f7f27f`
-	Default Command: `["perl5.43.9","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 17:11:30 GMT
WORKDIR /usr/src/perl
# Mon, 23 Mar 2026 17:18:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.9.tar.gz -o perl-5.43.9.tar.gz     && echo 'aec72b03806f2003f97e86baf28a22a20cce912d618afadf3df1f005cda5b235 *perl-5.43.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.9.tar.gz -C /usr/src/perl     && rm perl-5.43.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Mar 2026 17:18:12 GMT
WORKDIR /usr/src/app
# Mon, 23 Mar 2026 17:18:12 GMT
CMD ["perl5.43.9" "-de0"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12ca2afff00f3aa793396a5e0aa1a9bf514653514033e1666773eed2b58fa60`  
		Last Modified: Mon, 23 Mar 2026 17:18:29 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1304348ebb0ac22b01a3937f8ae5ea47e2c6d9c33fe992bc99116d3ed97e7a91`  
		Last Modified: Mon, 23 Mar 2026 17:18:30 GMT  
		Size: 31.6 MB (31570174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8105f5bbdb282e8ef69dc2c96348a264762c52710b4b8f2dc29a60035b85c3`  
		Last Modified: Mon, 23 Mar 2026 17:18:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-trixie` - unknown; unknown

```console
$ docker pull perl@sha256:d15ed29a49782bbcc2b7a0ebedd1e1c1008c580bc0db66709f40915ad9145abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a6b5db93ff087910ee198ead8b66a517468321ba06fb714973519aed57f0f1`

```dockerfile
```

-	Layers:
	-	`sha256:3f2469eb058b4c2601b6c42b6d7f39f79628de92aa9585529f5a17874d8ba836`  
		Last Modified: Mon, 23 Mar 2026 17:18:30 GMT  
		Size: 4.0 MB (4001778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40172ed40fbbbda99fe967a805a48e8403a4f4db1282914fe600dfc7a591b73f`  
		Last Modified: Mon, 23 Mar 2026 17:18:29 GMT  
		Size: 19.1 KB (19127 bytes)  
		MIME: application/vnd.in-toto+json
