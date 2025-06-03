## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:d5ab28564b1b67f7fe541bba4d5a1d4601eb75ea33f9b2a88b7d26d3b754f816
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:497ea4437136cd3b89ca91221e915c6d8da5a976688fdead6730679b3dd72cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274119215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2594d0adf5a2a5732997f98ef8e78ff0d7b0f18fa884b6545a03965fabd0c1e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd313a51460f26c1be869a155a8090af741c64ae9abd576f4e8645c10840416b`  
		Last Modified: Tue, 03 Jun 2025 05:16:30 GMT  
		Size: 144.6 MB (144635024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e29b0b4639236ebcb706ef0cb48c7e5f5342feba907590d25ff6400fc4523d9`  
		Last Modified: Tue, 03 Jun 2025 05:16:28 GMT  
		Size: 81.0 MB (80994904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e015a588e3ee3be154ced61d802c8cdccbf32700356e5e9fce786be888bf82f`  
		Last Modified: Tue, 03 Jun 2025 05:16:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e999be8041c3ddd923e5f148349da65a83f95e5f294aefd5c4da2afc2bc0816`  
		Last Modified: Tue, 03 Jun 2025 05:16:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4f2b3c3e824804b4fb453acc52b81c371bef418f47441aecf4ae0ac438102b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7234342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5233d8293bcad9dd21cf7aa8c4cfc92fb6f3a932fc2f3102c5107b02e2e3053b`

```dockerfile
```

-	Layers:
	-	`sha256:1663d4b7800f4657159ce51e34dcaa3c229c1dc0c14d753e70d385945a890f9f`  
		Last Modified: Tue, 03 Jun 2025 05:16:26 GMT  
		Size: 7.2 MB (7218522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009b73ebca43cb4e9293a52c0f26bf7b4f70f98af9ccecfea9c46f15680222a6`  
		Last Modified: Tue, 03 Jun 2025 05:16:25 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:86065b823a92c34d2558af3bab7bfde57c68327cd32b7de472a69ac306445df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272687487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b931156ebb8a394410ae40218cb602db835a1957bc7716018645837886e3bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010ef6cb6411a72cb9b7a87157534a1dd235611078bba6c262ef6f749557147e`  
		Last Modified: Thu, 22 May 2025 08:18:59 GMT  
		Size: 143.5 MB (143512648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab034bfe49534816a44f7956333671df05a572e02d89a83ab18c61d8c0752b0`  
		Last Modified: Thu, 22 May 2025 08:25:08 GMT  
		Size: 80.8 MB (80846620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3164fbc1f984b17e42e45d9eae92ea625cadcd0398caa308748a83756d5cec`  
		Last Modified: Thu, 22 May 2025 08:25:06 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea257e22b6c717319c046d6ec97e9aa4c1f8c1c0bcb412d640f988ef53985bc`  
		Last Modified: Thu, 22 May 2025 08:25:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:89f9d4b9bda1937373d7f5491894f0d1cdd49e5e82a885bd31c2f0919176e2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7240224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a724c3254f3dbfb9a2658e1c77d2487cd3387f1f120213dd4b3a91eb2b7afc2f`

```dockerfile
```

-	Layers:
	-	`sha256:ef46ce5e8f97c872d818f6cbc611ecc54965a86b33b555aba37c6bc053398e6d`  
		Last Modified: Thu, 22 May 2025 08:25:06 GMT  
		Size: 7.2 MB (7224285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c573592f375492b03ee3be8b57d33bce57425a3b107069d228350fcb6edc31`  
		Last Modified: Thu, 22 May 2025 08:25:06 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:542b1f325425b52059b4f23c9c85b56fe6d31cd0e2d1269a47fb60a3a045adc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283422946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0c1de3cd247000f9abccbe1b2668d743a1a09157b4ab275cc6f04769b118fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5fca0800952ffd845ecae7a757898651fb9b497615be2e0d7662f4d7ff229e`  
		Last Modified: Tue, 03 Jun 2025 08:44:24 GMT  
		Size: 144.3 MB (144280554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c601c153c6345b87854e25e7eb4f7088ff2684544f7e8eeb31a7f93a5ab40`  
		Last Modified: Tue, 03 Jun 2025 08:54:48 GMT  
		Size: 86.8 MB (86809737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf7cc7df71963d1b9d0a5ae06ea07f7436143da57b1b739c1f407342d52021d`  
		Last Modified: Tue, 03 Jun 2025 08:54:45 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98591661093e142128b40f3b9a4278c546ba98ba9aad77254522f8f6ebbd1688`  
		Last Modified: Tue, 03 Jun 2025 08:54:45 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:629fdc55cbc04abe099bbdcd989e4e699c75be9bc51e29e3183a3992de754763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7239595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bacc9820f2803006f1700a8e54801b084bb897c8fc56d326d1a16ccafb57aef7`

```dockerfile
```

-	Layers:
	-	`sha256:47509c9c5075513233f3ea72137afcace725bfa9e5b244c8af675e0a4b051745`  
		Last Modified: Tue, 03 Jun 2025 08:54:46 GMT  
		Size: 7.2 MB (7223726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc818f7e3de2eefafa2dd51ddfa7dba5710e5ce11e0e7be02d7c64d59864cb5`  
		Last Modified: Tue, 03 Jun 2025 08:54:45 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:75406eb551b30bf97e45de0bdb06c3cadcd34676d5c4d6de302e0894e246bcb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261607955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964e8ba541ed119497d4105b65b62b0fbf3f615365efe983ef6d837d081663ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f22e4165e784cf5cf4630de4aad9261205dcd457d5c03fd507e8f308626656`  
		Last Modified: Tue, 03 Jun 2025 06:12:24 GMT  
		Size: 134.7 MB (134673548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca254d7b13bff31aaa76d63b3e655b833ed2573527b8ca72855b0c9aca1310a`  
		Last Modified: Tue, 03 Jun 2025 06:18:24 GMT  
		Size: 79.8 MB (79789528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c14c5a1a3ddc964f11e265499db560401f7b9056a175d22d7ff76a430389200`  
		Last Modified: Tue, 03 Jun 2025 06:18:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a58776c1c2240b49ed641deaf29efd289ace4c5c9f07960c9817d9a32c45925`  
		Last Modified: Tue, 03 Jun 2025 06:18:23 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cdade843c0de9be28be286774ab9ba7af04b9c745f878dcf7ea4ddd7a28fc5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7228554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4aee6caa8a120cb22e501557f318245ca8dd01a0dfcae604a0d0dc707b85826`

```dockerfile
```

-	Layers:
	-	`sha256:7374b5650a2eb06799bd204b34c423f930c735ed276ef4899331ec2f286a01a7`  
		Last Modified: Tue, 03 Jun 2025 06:18:23 GMT  
		Size: 7.2 MB (7212733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f2ccf0609a282415ed6182fee5ba5b294eb33baf2c992ced1f188ba8af30db`  
		Last Modified: Tue, 03 Jun 2025 06:18:23 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
