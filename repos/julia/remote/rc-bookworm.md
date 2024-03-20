## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:c8cd39ef7e00dd53526453c6474ebd60f1bacc38728c36c628c8954cfdd595a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:rc-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:3607a4f1d507ef271c4290e10bec864c044e6ade11c5e719044c11789729f65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291431210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cebe68f1af0dbb37d8edd350f70f4b2817db3f946ddec18b92c4f0a359314b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 Mar 2024 17:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha2-linux-x86_64.tar.gz'; 			sha256='173044a594847c9d1b2067ae616e9923acf1989d5650f668eedfa7f377edee17'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha2-linux-aarch64.tar.gz'; 			sha256='1727138eae5712d2b51a92428f19304121a7fcf8d298684bfc99c538f56fb609'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha2-linux-i686.tar.gz'; 			sha256='449e4d80b9cf73ffa161cc96c3798404e2d1516f48e2545132f28b0600cf6df8'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha2-linux-ppc64le.tar.gz'; 			sha256='3391afb9fc930b129ccea11e5510e672852e387c4f23d6f12818e605702b1a0f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2229ed498de813f7785879a1b02dcdd822840f84f351dace9581495dc3ff07`  
		Last Modified: Tue, 19 Mar 2024 22:49:34 GMT  
		Size: 5.7 MB (5707866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d646b6bd4dd17c89b9da2fdd8436f3403bc9d2ea907a304ffac8470361bfd9`  
		Last Modified: Tue, 19 Mar 2024 22:49:38 GMT  
		Size: 256.6 MB (256598794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2824f5a433a2369b8121632f8dbf1aa3ab10ef0e3bc9e0db80e647b8ed794f1`  
		Last Modified: Tue, 19 Mar 2024 22:49:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a217e99a11336c02b49578381596f0773b6a15df513d251be65da44a9adc0a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a82c7f31e4ae695c0a0cc6162c9344010b42ecc9cff5c955966d463d036f3bb`

```dockerfile
```

-	Layers:
	-	`sha256:695207e1948a98ce325b13caac25afdac2fc6d24a05bd38dc2354198c463d7d2`  
		Last Modified: Tue, 19 Mar 2024 22:49:34 GMT  
		Size: 2.5 MB (2464878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406bbce5d11956d2c211dbfda56a2e67cf1621cfb917a37a81c87cb61956a6d5`  
		Last Modified: Tue, 19 Mar 2024 22:49:34 GMT  
		Size: 18.9 KB (18934 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8ada440f44f96c1e4e57bb9bfcb5e82970d43807a1de59f39bd094e747eb90e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289965418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20722f8780344bd62b11db66ea36c0d8b9453b73cd6fea690f67cc4cf25b130f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 Mar 2024 17:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha2-linux-x86_64.tar.gz'; 			sha256='173044a594847c9d1b2067ae616e9923acf1989d5650f668eedfa7f377edee17'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha2-linux-aarch64.tar.gz'; 			sha256='1727138eae5712d2b51a92428f19304121a7fcf8d298684bfc99c538f56fb609'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha2-linux-i686.tar.gz'; 			sha256='449e4d80b9cf73ffa161cc96c3798404e2d1516f48e2545132f28b0600cf6df8'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha2-linux-ppc64le.tar.gz'; 			sha256='3391afb9fc930b129ccea11e5510e672852e387c4f23d6f12818e605702b1a0f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5098140185724807fb3ae8d8fca309442f07fc1d338555bed7dbe965240c16`  
		Last Modified: Tue, 19 Mar 2024 22:52:07 GMT  
		Size: 5.5 MB (5533139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b89f788297080786551f001d2eae3e80537bf64933d71fa1877aed605fcac1`  
		Last Modified: Tue, 19 Mar 2024 22:52:12 GMT  
		Size: 255.3 MB (255275473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c9af03dc3f96cd2e4635c0fb2c6999482e7fb5786b95249083d579f5a4fca8`  
		Last Modified: Tue, 19 Mar 2024 22:52:07 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b432a66d2b86090c2867ed9c24645464c7db03941066d7ab5f836d03f50da708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a333a7b7b41f14ba101d2ea5063c00f5a5b7390816c9909754fcbd5f5f00e3f3`

```dockerfile
```

-	Layers:
	-	`sha256:8c0be4a4b1b58c8538515e84cc79486d117af4bd4edc16d98cef1259f685cdb9`  
		Last Modified: Tue, 19 Mar 2024 22:52:07 GMT  
		Size: 2.5 MB (2465111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:372645573e99b702c25eec9b9b9da35d0372471568b992ac0c93af2e9397ddf6`  
		Last Modified: Tue, 19 Mar 2024 22:52:07 GMT  
		Size: 18.8 KB (18781 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:66c62af7d04b3847c54178ed41569e5d07e08969c6ba7c397fa558476f828b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270445024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c4735b74b53bc73a8a2b14ddfd4d16b9c572ae0a67de128d5e898f8ec9d2bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 Mar 2024 17:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha2-linux-x86_64.tar.gz'; 			sha256='173044a594847c9d1b2067ae616e9923acf1989d5650f668eedfa7f377edee17'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha2-linux-aarch64.tar.gz'; 			sha256='1727138eae5712d2b51a92428f19304121a7fcf8d298684bfc99c538f56fb609'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha2-linux-i686.tar.gz'; 			sha256='449e4d80b9cf73ffa161cc96c3798404e2d1516f48e2545132f28b0600cf6df8'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha2-linux-ppc64le.tar.gz'; 			sha256='3391afb9fc930b129ccea11e5510e672852e387c4f23d6f12818e605702b1a0f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9663239fc7a77c1b7bf00c144732cc09b0b2880aa5e91603e182bdf06b2def27`  
		Last Modified: Tue, 19 Mar 2024 22:49:31 GMT  
		Size: 5.9 MB (5863229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1c4713c5b29ef17f0772b2e089fe392cf8e006784fe782e1a27ca01b929514`  
		Last Modified: Tue, 19 Mar 2024 22:49:36 GMT  
		Size: 234.4 MB (234439550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd3f3205c56c67fe4667e119cfdf742bafa2c1fcaef845e06815948b6c4159d`  
		Last Modified: Tue, 19 Mar 2024 22:49:31 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:826a939feaaea088c331b1537831d32614443475f989e379500d0b8c4cab42af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2480853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb14ff1755270c95d023556003711acfd515104568aceff77100e2d999324d83`

```dockerfile
```

-	Layers:
	-	`sha256:05fbc3b9ee1a7eb7442315e6d088a5a080a30200eb560d7722ce5b2949624f38`  
		Last Modified: Tue, 19 Mar 2024 22:49:30 GMT  
		Size: 2.5 MB (2461960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c1bf4a21f55b569b6af0702d7e332818a12e48c5cfc141c6e96830925c85f7`  
		Last Modified: Tue, 19 Mar 2024 22:49:30 GMT  
		Size: 18.9 KB (18893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:5c5610566259355102314f365937ff00e8dcd65f3afa7d80be87c73da7ffb3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283682915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0b7df4ad12ae38e4c6f7e9dcba6fc06aaeaa5adfecad68ddf7da00ce39dc46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 Mar 2024 17:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha2-linux-x86_64.tar.gz'; 			sha256='173044a594847c9d1b2067ae616e9923acf1989d5650f668eedfa7f377edee17'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha2-linux-aarch64.tar.gz'; 			sha256='1727138eae5712d2b51a92428f19304121a7fcf8d298684bfc99c538f56fb609'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha2-linux-i686.tar.gz'; 			sha256='449e4d80b9cf73ffa161cc96c3798404e2d1516f48e2545132f28b0600cf6df8'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha2-linux-ppc64le.tar.gz'; 			sha256='3391afb9fc930b129ccea11e5510e672852e387c4f23d6f12818e605702b1a0f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343ac94481c1fce7acc63eef8340c59008fd662b7dd35e8c8e83c4b0b5ae7208`  
		Last Modified: Tue, 19 Mar 2024 23:11:59 GMT  
		Size: 6.2 MB (6239922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1deffa9a0119bb8f3b97eda677569cc3fa449f93da70c4a6c3fd5d829b147e7`  
		Last Modified: Tue, 19 Mar 2024 23:12:05 GMT  
		Size: 244.3 MB (244323602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93c82a4c4dd39308065a8281b8dbe8938c704e7f4487e397c0cee08ec5948cf`  
		Last Modified: Tue, 19 Mar 2024 23:11:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:170316ef83f99cf5f395f1e4cd6768e4d9cbad058f0ba783b10a0f98c55ea61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48ed189bfca45f8933b0d57a2ffc2cbd7d88ea99a0a7a2507f5493aa49f68c9`

```dockerfile
```

-	Layers:
	-	`sha256:97e48039a84e7f20a3618b7a37f6b2c86ec8e10311d0d5ef3455d9ddc8136f53`  
		Last Modified: Tue, 19 Mar 2024 23:11:59 GMT  
		Size: 2.5 MB (2469297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53518a7566681752877918db7647ca5b0e427aadc5d9f89b3c4c132279d9e5fe`  
		Last Modified: Tue, 19 Mar 2024 23:11:58 GMT  
		Size: 19.0 KB (18986 bytes)  
		MIME: application/vnd.in-toto+json
