## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:fb14d2df3f54baa20649321e1858dc453438b0abeaebfc4ff8e886717e064b95
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
$ docker pull julia@sha256:86b93649c7937db5a3e078865c6e078a59482d8ce0fe1247be748f6ed167baa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191164689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9012484b46e60f9addfcfbb7b0796da0f3c83e571b4b7dd9386b4567f9419e72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 18 Dec 2023 21:28:57 GMT
ADD file:e9c344f1bffba57e46b30e3c70e4247dcf2e9d3e0484b2768f83ffd789bf3686 in / 
# Mon, 18 Dec 2023 21:28:57 GMT
CMD ["bash"]
# Mon, 18 Dec 2023 21:28:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 18 Dec 2023 21:28:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_VERSION=1.10.0-rc3
# Mon, 18 Dec 2023 21:28:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-rc3-linux-x86_64.tar.gz'; 			sha256='cb68ef2ebff2cfd18c1cba2c1ad8f37e73685ae6a24dbc036dfc86b2e13e0a18'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-rc3-linux-aarch64.tar.gz'; 			sha256='dc0baea6e9a7a1ec608b641d0658f1621a471b602b13a0facb72e0b83ccc8e6d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-rc3-linux-i686.tar.gz'; 			sha256='ac6938aab1d824029bf60959f80c3da7bbb5660aa32e9e97a5f7269a5c5c3986'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-rc3-linux-ppc64le.tar.gz'; 			sha256='45a499f7de8fabe5321469d3912a1b9bcddc15b3ddcc6c1671a5754f36a0e2e9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0-rc3","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0-rc3?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 21:28:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5808d881ded1b1deb8675903e6776c5a725d22c8a5c1061a96c74338f07591f`  
		Last Modified: Tue, 19 Dec 2023 01:44:31 GMT  
		Size: 32.4 MB (32402688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b7f7ee756eecf62119e4fe26ff3cd6a2ab101d24905d0c288d8337051a2fb2`  
		Last Modified: Tue, 19 Dec 2023 03:47:55 GMT  
		Size: 2.3 MB (2328882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b045981a1bf8eddb350759a29f6619a5aee807899a0bbb72edb634b4e6c21e8e`  
		Last Modified: Tue, 19 Dec 2023 03:47:59 GMT  
		Size: 156.4 MB (156432749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7b4f78b60bbf59966eed71512ba1ba0e8c6db2ee02a6c247cd8653620b62ca`  
		Last Modified: Tue, 19 Dec 2023 03:47:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f6de0c77f51a8a67bab60bf81f0aa469431dba67be03fd5cee9bd7c67fbefc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 KB (17737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f771e74bdd3dc598ea810c3c438adc0656fc58775d823557a9fd2367986ae7a0`

```dockerfile
```

-	Layers:
	-	`sha256:92c0f2997401ae91dc60b2a28f24b0752823ebb82a5a2a74b79dcba25732dfd2`  
		Last Modified: Tue, 19 Dec 2023 03:47:55 GMT  
		Size: 17.7 KB (17737 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:44a376483d613529b9845417436c8de5cb79b32bc7da91663146b75b26c63089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191624971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145954f62901044debdda0d615be5066b9a53a898a524a0aab1b6bf6e7da65a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 18 Dec 2023 21:28:57 GMT
ADD file:1cb772a6ad8ca6301624db3141029490564de7673bc0f2d4bedb5a1578ea85bd in / 
# Mon, 18 Dec 2023 21:28:57 GMT
CMD ["bash"]
# Mon, 18 Dec 2023 21:28:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 18 Dec 2023 21:28:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_VERSION=1.10.0-rc3
# Mon, 18 Dec 2023 21:28:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-rc3-linux-x86_64.tar.gz'; 			sha256='cb68ef2ebff2cfd18c1cba2c1ad8f37e73685ae6a24dbc036dfc86b2e13e0a18'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-rc3-linux-aarch64.tar.gz'; 			sha256='dc0baea6e9a7a1ec608b641d0658f1621a471b602b13a0facb72e0b83ccc8e6d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-rc3-linux-i686.tar.gz'; 			sha256='ac6938aab1d824029bf60959f80c3da7bbb5660aa32e9e97a5f7269a5c5c3986'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-rc3-linux-ppc64le.tar.gz'; 			sha256='45a499f7de8fabe5321469d3912a1b9bcddc15b3ddcc6c1671a5754f36a0e2e9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0-rc3","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0-rc3?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 21:28:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9f6fac7f65cfc65b7f8de8bc377b135ca95e45a3246cf2bd1bb90922679553e`  
		Last Modified: Tue, 19 Dec 2023 01:27:11 GMT  
		Size: 35.3 MB (35293807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dba17251d7ebde32646c984e46b9b02b6f3d7ab559026ad8fd99e5663840030`  
		Last Modified: Wed, 20 Dec 2023 08:36:54 GMT  
		Size: 2.4 MB (2425477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bbcd8fc6a2dc1eeafe8d12944a6b933377115a86bae8e4506df21c62cd3bf9`  
		Last Modified: Wed, 20 Dec 2023 08:36:59 GMT  
		Size: 153.9 MB (153905317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134cebb40e70f7f52d841c34b032c5d18ba5e0902cc099ea41bd885525949788`  
		Last Modified: Wed, 20 Dec 2023 08:36:54 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:4da04c421259e54e780a3b52c6e476155d40d750fffa58e48c6d428b4361642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b7e8bd7a14a3c6ed65411937ee506cacdabf2cfb725ef429363c0b02e809a8`

```dockerfile
```

-	Layers:
	-	`sha256:e0df90fc412c84c2bfa93bbdf6816c439e795df5f4a65936b345e95c14bac615`  
		Last Modified: Wed, 20 Dec 2023 08:36:54 GMT  
		Size: 2.2 MB (2235622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9e7199e7fba2bec18232f3f875d8499e304d959ab1004ca28491f628d0df14`  
		Last Modified: Wed, 20 Dec 2023 08:36:54 GMT  
		Size: 17.8 KB (17846 bytes)  
		MIME: application/vnd.in-toto+json
