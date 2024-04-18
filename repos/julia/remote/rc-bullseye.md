## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:6625b054b678e97022b20185b806b7b7f47a80d0baeffa90cc0ffb82644bfc6d
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

### `julia:rc-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:bd2104b36fd7cfe1feee1b0c8ce1d958e37a2448eaa318d3a8e2f894e222bce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (290974402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcb7377236b37680cef8effaea3a3c2768828e2b43c1e19953ad4bc0b97675c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 10 Apr 2024 21:26:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta1-linux-x86_64.tar.gz'; 			sha256='43aeebbad319dc9153d3683c39bc2c07dd2d500817d6114e901eb590fd47c472'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta1-linux-aarch64.tar.gz'; 			sha256='9e2ce232e40d2e946440cbaa3fc3dd4a51033021bbef7fb5bc2ac62fff8e44fc'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta1-linux-i686.tar.gz'; 			sha256='966f9d461d6e854973895f8ad11ea62b38378d475479b58c8e792f6f50c6c026'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta1-linux-ppc64le.tar.gz'; 			sha256='7b3ecc6e001c80243e71b72594fba4f713cdd14abbc19d3d57d386dd1c252746'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-beta1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-beta1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 21:26:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f02bf7164f595401fd2184eb24bd27daac6a7cde587280f55e8392d6a4a383`  
		Last Modified: Wed, 10 Apr 2024 23:57:14 GMT  
		Size: 2.4 MB (2426547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd676c2661e2906aa97b748d79a4b127f40924716d88d30b476486929bf5fe91`  
		Last Modified: Wed, 10 Apr 2024 23:57:19 GMT  
		Size: 257.1 MB (257119745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96af86205e67e81bb5551c96f54413f18728c5636bfee7ebda8c527cd08249f`  
		Last Modified: Wed, 10 Apr 2024 23:57:13 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:636fd37946ee307662c41c81d74677519f0ad1af9573438cbc09e87cb7ceacd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e983c07625a063a26390bbcfa1ead1d4975127e0e0c00cf9db1ec3478f130c30`

```dockerfile
```

-	Layers:
	-	`sha256:a4ee7bd62426851d0f50a4e8b232a9aaa115556c473b3b31ccbf077ebec6954e`  
		Last Modified: Wed, 10 Apr 2024 23:57:14 GMT  
		Size: 2.7 MB (2680967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1fc4182f15b353e6ace939b778cff5e0f50a0388c1f07182b5983f2eadf4251`  
		Last Modified: Wed, 10 Apr 2024 23:57:13 GMT  
		Size: 18.0 KB (18021 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9af0c6fb851f5f352775876611c978062490aedb691a911362d9e74d3c7abd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288121727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d80c10d183f0d9e976170a443fdb8ff003a1d436885e46e1beee6fe34abc9b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 10 Apr 2024 21:26:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta1-linux-x86_64.tar.gz'; 			sha256='43aeebbad319dc9153d3683c39bc2c07dd2d500817d6114e901eb590fd47c472'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta1-linux-aarch64.tar.gz'; 			sha256='9e2ce232e40d2e946440cbaa3fc3dd4a51033021bbef7fb5bc2ac62fff8e44fc'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta1-linux-i686.tar.gz'; 			sha256='966f9d461d6e854973895f8ad11ea62b38378d475479b58c8e792f6f50c6c026'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta1-linux-ppc64le.tar.gz'; 			sha256='7b3ecc6e001c80243e71b72594fba4f713cdd14abbc19d3d57d386dd1c252746'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-beta1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-beta1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 21:26:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2908a0cb58c1f02a4a3a2d1542f497aa11397e3dffc1286841529c4f59c3e9`  
		Last Modified: Wed, 10 Apr 2024 16:33:49 GMT  
		Size: 2.4 MB (2415070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8199237556061df4d45ca26429d6a893ecf79273d18cbbf7ed274c1f90145ea7`  
		Last Modified: Thu, 11 Apr 2024 10:27:40 GMT  
		Size: 255.6 MB (255629978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51f1dcbced6b7c07c3c5d29f7e65ab742a9fdc7dc0e5fe26cbc3390edaa52fb`  
		Last Modified: Thu, 11 Apr 2024 10:27:34 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:46ba080edf655612a2606c614797cbf733573f6dca4bb2d432248dff76f01c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0314f622f2f309d0d37621dc4011cdf5bb7f67e17d3bad14463cdc2acd678d54`

```dockerfile
```

-	Layers:
	-	`sha256:14472ce3a82aa4a381e6f8b3cba67934d0ef839192ed2803ee7a769d205324ad`  
		Last Modified: Thu, 11 Apr 2024 10:27:35 GMT  
		Size: 2.7 MB (2681184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b210246a38e52e3d6be4b14d68502266380550c017e33e93655330d8d3124ef`  
		Last Modified: Thu, 11 Apr 2024 10:27:34 GMT  
		Size: 17.9 KB (17861 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:f3628375d5b318f92b44cad753b1b066d0b50d76fb3b5e5a6608570564c86a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269482490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fbc48aa73c966ff5b22f546b405ff2f065f1ab15050823c8de9726fc0551d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:34 GMT
ADD file:107da403005e1b6808da193b1f269be14ac31b0bd6d87b7609e9080e75f08eab in / 
# Wed, 10 Apr 2024 00:57:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 10 Apr 2024 21:26:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta1-linux-x86_64.tar.gz'; 			sha256='43aeebbad319dc9153d3683c39bc2c07dd2d500817d6114e901eb590fd47c472'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta1-linux-aarch64.tar.gz'; 			sha256='9e2ce232e40d2e946440cbaa3fc3dd4a51033021bbef7fb5bc2ac62fff8e44fc'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta1-linux-i686.tar.gz'; 			sha256='966f9d461d6e854973895f8ad11ea62b38378d475479b58c8e792f6f50c6c026'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta1-linux-ppc64le.tar.gz'; 			sha256='7b3ecc6e001c80243e71b72594fba4f713cdd14abbc19d3d57d386dd1c252746'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-beta1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-beta1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 21:26:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec8b01fa71b8466600831f50045cfc2951257ac6eee36ce2a0fbe3dbe0098d42`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 32.4 MB (32413416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007ee3477b15bb6ba7c36261aec19505bbadbb33dc861d2966527875cf7d7b23`  
		Last Modified: Wed, 10 Apr 2024 23:56:57 GMT  
		Size: 2.5 MB (2533043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030fd4ae33bcf7edd30209dcbe3389e78442f6748a505326635df80663753de9`  
		Last Modified: Wed, 10 Apr 2024 23:57:02 GMT  
		Size: 234.5 MB (234535663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afa040eb25cd56555efb6c138953b72638c88cf78ef12cde95760b73c29d3e9`  
		Last Modified: Wed, 10 Apr 2024 23:56:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b7dddc2dac81c100b596e24bb0256bbd8b1bab8f6eb1c7f1a275f01f05c6354e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3425bef628f46fb5ef473158c075d341132524607ab3a1715ec8590f2b23ad73`

```dockerfile
```

-	Layers:
	-	`sha256:1a9f1d8bf34b129e0c4e112750040abdae55cb71c9f591e4b79282c283479ee6`  
		Last Modified: Wed, 10 Apr 2024 23:56:58 GMT  
		Size: 2.7 MB (2678072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac34b0522eae1348e462de2a9477de833a81f4e80e322e2b65b710bf4fe3bc1`  
		Last Modified: Wed, 10 Apr 2024 23:56:57 GMT  
		Size: 18.0 KB (17995 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:5115532679166625228506d14c8a1e6b8bda578f7464e6d7ff97cd02f4773cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.7 MB (282720336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787c98fcb99e31ea3ffa134f76ec6cbc2f67494ea720121e10c862802e02177a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:00 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Wed, 10 Apr 2024 01:27:02 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 10 Apr 2024 21:26:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta1-linux-x86_64.tar.gz'; 			sha256='43aeebbad319dc9153d3683c39bc2c07dd2d500817d6114e901eb590fd47c472'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta1-linux-aarch64.tar.gz'; 			sha256='9e2ce232e40d2e946440cbaa3fc3dd4a51033021bbef7fb5bc2ac62fff8e44fc'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta1-linux-i686.tar.gz'; 			sha256='966f9d461d6e854973895f8ad11ea62b38378d475479b58c8e792f6f50c6c026'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta1-linux-ppc64le.tar.gz'; 			sha256='7b3ecc6e001c80243e71b72594fba4f713cdd14abbc19d3d57d386dd1c252746'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-beta1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-beta1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 21:26:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9607417039222013c1bc44bf8e4386bd854d0c08e059c2062318347a75107d2d`  
		Last Modified: Wed, 10 Apr 2024 19:18:34 GMT  
		Size: 2.6 MB (2629998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd432fc1d047b475d92f516a1cbcc791277d09c47080cc213ec4236dd4371f64`  
		Last Modified: Thu, 11 Apr 2024 09:25:29 GMT  
		Size: 244.8 MB (244785877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fda84b721acd4f7d8003be46479aa83cc81e59283febdc97a865c195f559a95`  
		Last Modified: Thu, 11 Apr 2024 09:25:22 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:dc60194877126ca45e93b2d406b90395ca30f79a7d4f6225287a7c7b03a7e248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a35e97ac97b4dfd1318aef55558124d5385477d33f1f5d4a699b5bdbaeefda`

```dockerfile
```

-	Layers:
	-	`sha256:45df1164a7c05bd3c1b94e6c4e2579a1266637c07778dd0058127482bc2dfbdc`  
		Last Modified: Thu, 11 Apr 2024 09:25:23 GMT  
		Size: 2.7 MB (2685358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fc1792a07b231d4fc440941185740bc0c6533ee5213707bbcf1fb8421781ea`  
		Last Modified: Thu, 11 Apr 2024 09:25:22 GMT  
		Size: 17.9 KB (17888 bytes)  
		MIME: application/vnd.in-toto+json
