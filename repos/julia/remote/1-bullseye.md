## `julia:1-bullseye`

```console
$ docker pull julia@sha256:a93ddde7a69f5a1970994656f8f7a1ed90252a6eacc7f2debac853ffd20a3a36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:8d384ae00c7c02cbee899728190fcdd1faca693ec80fed6d734c76a84922a118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204925804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19950a8b05c384b4f92d751f4f10a98e63aa069ead4d5cf9186b030c920da3a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f3f6d4871c74f7b63e34b697a9aaefa8835f1889dc6903866338a86317002e`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 2.4 MB (2426534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba72295cd998aea9729c2a415acf7f007a528c2b4d6f1c34387bb92d9bac746`  
		Last Modified: Tue, 13 Feb 2024 01:53:58 GMT  
		Size: 171.1 MB (171076476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d0425419406b5a1143dff3543f91ff035c7d0ecb9bf0774e64e01554e02e20`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8273a9fdda9b316a362eeb3ea1e578ee9092b278a30a718754a7c3a8deacd3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04952d04716e6ab86f7cf6f5e35bd7873721540b5380dd2811279304f811d7f4`

```dockerfile
```

-	Layers:
	-	`sha256:432180086c941804e7ee5fcf6bd251520e95f0fdb359e58e157794fe17baa0b4`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 2.4 MB (2359551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870a84f47d45ed4bb0321a5cc4914f58d0ee37c40ea0d352c1b840eaa8d48cca`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.2 KB (18186 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:5487dbd9e86ea6dfdde1e83477c820ef9096cbd52e19dcc574b6fd9efb76b2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196864925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80daa6ec8fc78a3eec97067ae5b96e344d99367cccefba598286c51b1386fdf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd381bc5ce074386a44640a70f3d2d53921e7cda7c6386a20616c9fab4cee5`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2415040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a7f557218cd3b5ef3f4ddd5afcca8d80438c186a9bf2521eda165facd2c91`  
		Last Modified: Wed, 14 Feb 2024 00:41:38 GMT  
		Size: 164.4 MB (164378442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268a60e13473050784334fa5d0cc23da2209b45f3251f0133c2c05c309d0b752`  
		Last Modified: Wed, 14 Feb 2024 00:41:33 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f8bb44f08113f3d1137034416ccf2f473631f08424eb97007061de4ac057ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951d6f2d9e6a3d58bcd7de98a60c4417e42eeafb974b36e71f6fb0760357a357`

```dockerfile
```

-	Layers:
	-	`sha256:7beff45e48bb073460b5214a082784914cd78b5c8864627f675670dff6784190`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2358903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2687ab055e0cc2332a76ad9df388d45043b631992252746a3b6d1260836fc41`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 18.0 KB (18028 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:3348a4e15f9eb821e27b64f594aee5b549605b9a02ce2d81bf0296660348dccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191411992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cc23d0f384f592a3f59a3d676eb76d72ea43b54725d5f8e0baeb644aebdffb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf492369ec4d56d2010213bf0c01a1d0be40c950eda27da51921ed8c2a1bc09`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 2.5 MB (2533067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d0f5baeea89d7b49c54cc577eab3867247693f466f98b3cc4f2399efcb0af`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 156.5 MB (156471113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6be2aecc9dc90a8f90619365daf78c2fc8f2c67056592b5b10683e9b84c892`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8016124e8b1742e9b8063df61bae834e255e72ef863ed54fde680195b00a6e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9820be04702fdac240a66ebb9fed36ff9a01b291501d69df9966aaa79cbb048`

```dockerfile
```

-	Layers:
	-	`sha256:b5b0fa0ccbf3afd955632b36296386d1988c6a60b808e7101b4b3f9320935cd2`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 2.4 MB (2356757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:427416a00deb6fc64dea6ac42ea75526fa410b61d0f98ed7c269e848697a670b`  
		Last Modified: Tue, 13 Feb 2024 01:53:53 GMT  
		Size: 18.2 KB (18155 bytes)  
		MIME: application/vnd.in-toto+json
