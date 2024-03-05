## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:4b80a7a2e071356ec452b8f97ff2f7369db905d1b17d298ebc0d4c35ad83fd24
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
$ docker pull julia@sha256:b9bb1b47a5a59dcd1ac9086e12e2ec67062a6b993c264999560454f795109574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282381882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00034855f6233f30320448ff4c95b6cc2662b73b5d613e30e997d6376ee6dfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Mon, 04 Mar 2024 21:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 04 Mar 2024 21:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_VERSION=1.11.0-alpha1
# Mon, 04 Mar 2024 21:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha1-linux-x86_64.tar.gz'; 			sha256='c8f08144ec2f1d4930dac19c884f840d985fd33fc70c2256a0fc8f0a85652056'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha1-linux-aarch64.tar.gz'; 			sha256='70f98026a210dfddd1a143145703ee6e2fb5eb9063a280e2d710eda0bb925d8d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha1-linux-i686.tar.gz'; 			sha256='511df786cf4e75d290bae6fcb2ab0d25c94482058690cb424934117993bac21c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha1-linux-ppc64le.tar.gz'; 			sha256='c731dd05ef3aaa9245dd860fb8ec2f3df65035107fcd1179b113584b13233f91'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac4e5e89c4176158b5d6907073cc6f783feafc347e42eba338f95b875206d3b`  
		Last Modified: Tue, 05 Mar 2024 00:50:58 GMT  
		Size: 2.4 MB (2426520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf7e34a0ea37b9851473698eb8c206422dd7e3095503cfea006408e9217c8e4`  
		Last Modified: Tue, 05 Mar 2024 00:51:03 GMT  
		Size: 248.5 MB (248532568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d60fc6c0f8142fa3d2d93d62fabb602706a4cd08d5bf5df6474a718496ef345`  
		Last Modified: Tue, 05 Mar 2024 00:50:58 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:acd3278489e7d64b80630865c51992a0ad3cae1f834979dfc2e929d49acd6c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fbc2971f9427da33f17dded4b87b9a620207d0988805e3ffe4c2649fce38cf`

```dockerfile
```

-	Layers:
	-	`sha256:78a93e5fe461aed2bf3b2c07ad6e9fac243435e6936f0e99cd943031c236d86a`  
		Last Modified: Tue, 05 Mar 2024 00:50:58 GMT  
		Size: 2.7 MB (2729573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4454e062e1a4f114eff78a9d717518e739b9e2b60b945d259e6a70f4a04addd2`  
		Last Modified: Tue, 05 Mar 2024 00:50:57 GMT  
		Size: 18.0 KB (18038 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:44b8dee715ba84abd7f0256c921245a77634fee93f5e4c72f4db62f0e7eb06f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273580612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761287f0c7695a89b61d47e1d23fc48646dfedc27bd994abdd9c37580f814193`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Mon, 04 Mar 2024 21:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 04 Mar 2024 21:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_VERSION=1.11.0-alpha1
# Mon, 04 Mar 2024 21:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha1-linux-x86_64.tar.gz'; 			sha256='c8f08144ec2f1d4930dac19c884f840d985fd33fc70c2256a0fc8f0a85652056'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha1-linux-aarch64.tar.gz'; 			sha256='70f98026a210dfddd1a143145703ee6e2fb5eb9063a280e2d710eda0bb925d8d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha1-linux-i686.tar.gz'; 			sha256='511df786cf4e75d290bae6fcb2ab0d25c94482058690cb424934117993bac21c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha1-linux-ppc64le.tar.gz'; 			sha256='c731dd05ef3aaa9245dd860fb8ec2f3df65035107fcd1179b113584b13233f91'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:21:28 GMT
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
	-	`sha256:3a39124e877574dd781ed7a9ee14f56dbaa046e2c1c0e26f471a519f67600cb8`  
		Last Modified: Tue, 05 Mar 2024 00:57:31 GMT  
		Size: 241.1 MB (241094122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b3104199e6682ec92c0598cb8218921041430be46967a7b9bdeedd51ce848`  
		Last Modified: Tue, 05 Mar 2024 00:57:25 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:278205265b2307efcbc8cc13eb2ee9f516a58536a8950f5b1ce45e60e7a1d307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf11565266707401224e919bebfd49b6b2db3c47db6e943e4e4a62657296961`

```dockerfile
```

-	Layers:
	-	`sha256:664d6e981c0a2851b10bb86330e401dba0b827f6bae165d64c2901b877a35239`  
		Last Modified: Tue, 05 Mar 2024 00:57:26 GMT  
		Size: 2.7 MB (2729790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49eba9ef9ae8a557c393d7b198fb79b9053381def767329ab72fcea087006f6d`  
		Last Modified: Tue, 05 Mar 2024 00:57:25 GMT  
		Size: 17.9 KB (17879 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:88aa694f60f9e72cc03559697d7817e71ef7da6ded49566c1d600c4304c2924d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265447303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96b69e4853ed76c50548d2b1bcd25c578d309acc7e4db020279bbe7b5ad96e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:18 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Mon, 04 Mar 2024 21:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 04 Mar 2024 21:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_VERSION=1.11.0-alpha1
# Mon, 04 Mar 2024 21:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha1-linux-x86_64.tar.gz'; 			sha256='c8f08144ec2f1d4930dac19c884f840d985fd33fc70c2256a0fc8f0a85652056'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha1-linux-aarch64.tar.gz'; 			sha256='70f98026a210dfddd1a143145703ee6e2fb5eb9063a280e2d710eda0bb925d8d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha1-linux-i686.tar.gz'; 			sha256='511df786cf4e75d290bae6fcb2ab0d25c94482058690cb424934117993bac21c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha1-linux-ppc64le.tar.gz'; 			sha256='c731dd05ef3aaa9245dd860fb8ec2f3df65035107fcd1179b113584b13233f91'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68554917167d38ac292229bfde7f147daf476386a801d8152a1ee2fba3e5ea5e`  
		Last Modified: Tue, 05 Mar 2024 00:50:18 GMT  
		Size: 2.5 MB (2533056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1bb50e3d9062469082181ae13f94d7601dcf2aed58a37722360a8e6c00f11b`  
		Last Modified: Tue, 05 Mar 2024 00:50:24 GMT  
		Size: 230.5 MB (230506433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8650c431b20c9a21c9958b6f6962a2e54935b2916b9bfa92c17e8bf3e7a717`  
		Last Modified: Tue, 05 Mar 2024 00:50:18 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:7e4e3e8ada6c912e56ff43b09afa1de2aef3e7d0463786043cb359639b0ea987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2744690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5044ab3462d92f9ed69d767f1c05ba173116d508b2fca40e57f612b5e4b2e516`

```dockerfile
```

-	Layers:
	-	`sha256:d51477f640e66d2be8fb0664ab5d9ec43f6cf35ddffcb2fe4c4bd4e55d64018e`  
		Last Modified: Tue, 05 Mar 2024 00:50:18 GMT  
		Size: 2.7 MB (2726678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2390d490e20f50c6610d4f277b95515289e8e809cfdaa613532553397c308fa5`  
		Last Modified: Tue, 05 Mar 2024 00:50:18 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:b223704cf779ef2626195da6ba8b12ad8d128e424075c6642e784ba14adb19a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.0 MB (279042673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad65297eba5a6413ea8f3d2841d98df8811fdb96ab1d4d6d846c916263b79f08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:33 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Feb 2024 00:39:36 GMT
CMD ["bash"]
# Mon, 04 Mar 2024 21:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 04 Mar 2024 21:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_VERSION=1.11.0-alpha1
# Mon, 04 Mar 2024 21:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha1-linux-x86_64.tar.gz'; 			sha256='c8f08144ec2f1d4930dac19c884f840d985fd33fc70c2256a0fc8f0a85652056'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha1-linux-aarch64.tar.gz'; 			sha256='70f98026a210dfddd1a143145703ee6e2fb5eb9063a280e2d710eda0bb925d8d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha1-linux-i686.tar.gz'; 			sha256='511df786cf4e75d290bae6fcb2ab0d25c94482058690cb424934117993bac21c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha1-linux-ppc64le.tar.gz'; 			sha256='c731dd05ef3aaa9245dd860fb8ec2f3df65035107fcd1179b113584b13233f91'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha1?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc406362a4b5aed4760caff7c4bc06a04cb2bd3834a923f056a5baf70eb0d7ff`  
		Last Modified: Tue, 13 Feb 2024 21:56:31 GMT  
		Size: 2.6 MB (2629991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9adad0513243c4ac6878bb3bce3f1e4eeff95df31803936eae68c880291414a`  
		Last Modified: Tue, 05 Mar 2024 02:24:54 GMT  
		Size: 241.1 MB (241114512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe10b5de21d6196e66613daa4542ce0128db2520f65df46f95988df574b2ae`  
		Last Modified: Tue, 05 Mar 2024 02:24:48 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:c38ed4819527d8216ea3250edf6e3e308783080f635ef911dcfe0fb4eb2b1a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b263b9cfc9cf6c37a7775f2c4e14913550a845ca88a26a3164e13bebaefa936e`

```dockerfile
```

-	Layers:
	-	`sha256:3c6552a94bcbc2bfa82963935737f1fc3443af81f3fa1cf43e8e5c89283f6a9f`  
		Last Modified: Tue, 05 Mar 2024 02:24:48 GMT  
		Size: 2.7 MB (2733964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417fae934aa211ecc99cfab2bc0b325bdca4e90948326fc15a2487bd268e5392`  
		Last Modified: Tue, 05 Mar 2024 02:24:48 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json
