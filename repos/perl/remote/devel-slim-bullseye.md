## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:5def69f7c4f1e71e6c58ea6784f6a2ad7b8e5b3249dfe0c81f3d72e6c62b7363
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

### `perl:devel-slim-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:08587195692be97f5768bb8b1401f6354d280c3928db986fe549a678f4e2d407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56695373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d805a9f282b0d0ccfb873512677d390717a2ea9a710f452f88f38cc525dcd33`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:55:54 GMT
WORKDIR /usr/src/perl
# Mon, 16 Mar 2026 22:59:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 16 Mar 2026 22:59:59 GMT
WORKDIR /usr/src/app
# Mon, 16 Mar 2026 22:59:59 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d404c6e3de50d12b7bd59c67d9684337877071b8c0273ea6edfca51677fae097`  
		Last Modified: Mon, 16 Mar 2026 23:00:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9311fac740a687885626ff1d46135007d624cc09fa1fdc01cf43a4a96656164c`  
		Last Modified: Mon, 16 Mar 2026 23:00:14 GMT  
		Size: 26.4 MB (26437283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b611fe2d6b9e493b9035dfed7ebb311a57924bb61a45b50fb6136b50e8d10a`  
		Last Modified: Mon, 16 Mar 2026 23:00:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:622870f78f86cd0ee65f58c3d0b43f9ce354830b2ed9bae9ff23bfbd658cb9c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4147307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139c8d309b6f76a6674d9a58ae77f2028f2b1d377a3b059984e4213b498deb53`

```dockerfile
```

-	Layers:
	-	`sha256:ac325246921a65471cbdc6894f6df73eeba16bfec2eb9a7128b66c3000a7edf3`  
		Last Modified: Mon, 16 Mar 2026 23:00:11 GMT  
		Size: 4.1 MB (4129063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98caf5d2da8f00e20beb6b28175a52fe9848ef40429be7707ba63de04393b320`  
		Last Modified: Mon, 16 Mar 2026 23:00:11 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:e12a9f1b50fd738ddd51a8d071d90581d2c8edf24f8ebc3486632963058a7fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49239943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa53dbe71fdcd4579d14366c17f2f8cc6654d6daf3b1383d79405558c3c669e`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 00:02:59 GMT
WORKDIR /usr/src/perl
# Tue, 17 Mar 2026 00:08:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 17 Mar 2026 00:08:30 GMT
WORKDIR /usr/src/app
# Tue, 17 Mar 2026 00:08:30 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:3bc17afcb32786a635d7faf13a7aa3a4142ac1a648b659c697f5e02460592774`  
		Last Modified: Mon, 16 Mar 2026 21:52:44 GMT  
		Size: 25.6 MB (25551392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d5aae345ea1bd07cf5a9f367b36d377f060f3796785c7f2aa8ce799f62430c`  
		Last Modified: Tue, 17 Mar 2026 00:08:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa30e4180c10f1a62527fd40bd440c564b21e7c91f50a354977c48679c1d4e1`  
		Last Modified: Tue, 17 Mar 2026 00:08:41 GMT  
		Size: 23.7 MB (23688286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a680cb6b9e9d498408b3fbea8baadb6a7810a07e26064abfe6b1f0cccfae34`  
		Last Modified: Tue, 17 Mar 2026 00:08:40 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0cfb6a98756f85ec49df8d06beb8a9990df40cddb321aceb08164331f76f7c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f967544f2a14bbce35999c16552caef2fc6bb5504e1671539c8e6144787a53e`

```dockerfile
```

-	Layers:
	-	`sha256:e82eb0f459669e60f98941ef51a0bacb58f3fcfad8c9f722d6d5060712508be1`  
		Last Modified: Tue, 17 Mar 2026 00:08:40 GMT  
		Size: 4.1 MB (4103052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e42589e092dc9c2dc296a148ecde4522c28144a63035265d04395d58066654c`  
		Last Modified: Tue, 17 Mar 2026 00:08:40 GMT  
		Size: 18.3 KB (18316 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:0690701c05fe1c56a5fb9e3f324ce45179351d96cf726d669d312362290d0bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54304845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4994755669bce857179127fd75f4df04a267c44be2cb47895be383f25e6c311b`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:58:22 GMT
WORKDIR /usr/src/perl
# Mon, 16 Mar 2026 23:02:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 16 Mar 2026 23:02:58 GMT
WORKDIR /usr/src/app
# Mon, 16 Mar 2026 23:02:58 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c517c5af6e185a90e4f3f3358a9e24f1da2cc2abce738980a727fd2ec086eaae`  
		Last Modified: Mon, 16 Mar 2026 23:03:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250d3c28197ad7f07a964558fbf746271fac12581d9f7832d13ea77352d3ce33`  
		Last Modified: Mon, 16 Mar 2026 23:03:09 GMT  
		Size: 25.6 MB (25560054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a69fbcd91ff0cdfe24a90c77bb29404c6d58f2b00a1da3ec9f7d19a7907b7d4`  
		Last Modified: Mon, 16 Mar 2026 23:03:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c0b7661a7a921b82f15614f6c2187061a122b4758b9346d9d2a9f3deae95ffa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c883682aff7fee8132ecf470200d35a3a8c138e01b39a122decd7f00bd3345c5`

```dockerfile
```

-	Layers:
	-	`sha256:2bde1842028892bd5661c4913834fa2716e49ad0705a3b9bb220011809d0eedc`  
		Last Modified: Mon, 16 Mar 2026 23:03:09 GMT  
		Size: 4.1 MB (4103458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6dc263e27505f7bf4fd803c6bd42198e7f4b5291624de898c14abac1f62f01`  
		Last Modified: Mon, 16 Mar 2026 23:03:08 GMT  
		Size: 18.3 KB (18335 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:8082afbfe37f692af38a320a862580c0da6ca382be2f53f8c1c87a2d16b9c07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59138800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e5b1c00f04c1e53e35356ba5b77786ec82443729bc47696bdc6330a3e21289`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:51:13 GMT
WORKDIR /usr/src/perl
# Mon, 16 Mar 2026 22:56:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 16 Mar 2026 22:56:13 GMT
WORKDIR /usr/src/app
# Mon, 16 Mar 2026 22:56:13 GMT
CMD ["perl5.43.8" "-de0"]
```

-	Layers:
	-	`sha256:f9a1ac4759c4f531107bbcb94882648bc1b2c093ca00c3ddc1fe3d72957fb19a`  
		Last Modified: Mon, 16 Mar 2026 21:57:07 GMT  
		Size: 31.2 MB (31191663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1b9b6d5915b732318e4e0bea8ebf940ca830b86e1037101076d17a87ecd0ea`  
		Last Modified: Mon, 16 Mar 2026 22:56:23 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8b661deea506a491e33d81b08ea9fe8dd526628818d4d489cb6ff5277f398f`  
		Last Modified: Mon, 16 Mar 2026 22:56:24 GMT  
		Size: 27.9 MB (27946874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebb8c3be72dced4aa81045ed30208e33e0e33118847a006ce4628496a8eea7f`  
		Last Modified: Mon, 16 Mar 2026 22:56:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:df485c8711b201c31fd8b5aecf42fcab4ff4b39dc9b1988569ac2c8154a32098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdfb89f4152f057867e1efb7a9437bd30264b6e74d732b8bb722014535056b5`

```dockerfile
```

-	Layers:
	-	`sha256:8002e337fbf1c08b64389ab813c33817f453a273b802b88e58408d0ef15b0cc6`  
		Last Modified: Mon, 16 Mar 2026 22:56:24 GMT  
		Size: 4.1 MB (4133345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20e3cbb6bb18d4f75616aef767b03d523868f2cb008f871f33d8fb69bd54ff5d`  
		Last Modified: Mon, 16 Mar 2026 22:56:23 GMT  
		Size: 18.2 KB (18217 bytes)  
		MIME: application/vnd.in-toto+json
