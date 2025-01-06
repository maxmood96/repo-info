## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:0c730df14422ac29db246724e8a3ca95efb1a1231eb06d647d55086a8a67f50a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:517179d1198d9c2848201fb65ee58cbd6d2d0e49e9ccc35fb10adf85253f061c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286810561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0149bf344a8dee4a7f0c901603637d6572561e6deb95f0423af13b2f4ff8a930`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcc8fe8bea12ef84c9ee9d45ad9bf1cba448d62a029554a198100843d2997db`  
		Size: 157.6 MB (157568680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f222d4b2f22d1f47a8fc39f6f2df3f2a75f6f748969f5f18bd285f1865af27f`  
		Last Modified: Tue, 24 Dec 2024 22:38:26 GMT  
		Size: 80.7 MB (80743774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd23d89c097a61882e8e4e083c591f60b314f5b6b929c79260c3566fe4801a54`  
		Last Modified: Tue, 24 Dec 2024 22:38:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b43dab221e76a89a860cb888213798dcf895a64e4654082971129ab1d634c88`  
		Last Modified: Tue, 24 Dec 2024 22:38:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1c7956ff25e40562a7a33c8974808c93e47a1fb8fe81e5a3110d880c5541b25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30950b3815be7d90e543cc829732816bb48431f59025b876083e1c20f8098df1`

```dockerfile
```

-	Layers:
	-	`sha256:ccfb7642302f4a8ae3a75f9b0fb7c709caae8165b00a9eb0c716009c1062e941`  
		Last Modified: Tue, 24 Dec 2024 22:38:25 GMT  
		Size: 7.2 MB (7176120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d08dea2c35a9ff1a1baa86d37b5df3023bd6dfb97e5d103995a7cfbe471ab1b1`  
		Last Modified: Tue, 24 Dec 2024 22:38:25 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ebd5958ba0dec11a2589036797fcba5a27ad0cdbb1f8952a63341cdef957678a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284725006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b67697863eb0b0d97f3f403b3bd462349c8986c77ec0d8e176330d1bf462cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd80492bd56138294a3d10e9508d1eae93219173075ed84b75388a4bd08b9cb`  
		Last Modified: Wed, 25 Dec 2024 07:10:26 GMT  
		Size: 155.8 MB (155793105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb684ac100acefc0c5d7325ef85ff77ef1e199c9aec4117684d718ad19ea851a`  
		Last Modified: Wed, 25 Dec 2024 07:34:03 GMT  
		Size: 80.6 MB (80605379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2de98150f8885676aae31737bd7211f0246f9a360664615c861d8185b741f77`  
		Last Modified: Wed, 25 Dec 2024 07:34:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddaae1f53505c0b59b843541aef75beae706dccdae0334e3240fe87dac5b5c9`  
		Last Modified: Wed, 25 Dec 2024 07:34:01 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:963129ca6923acbb8eafb6927df650b5260986d7b8e0e861fa7ce8e6f48abe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7199966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e0bb184145ff74ae19b6540451b6ba354f75b5618ede6f2cdc8ea366577a43`

```dockerfile
```

-	Layers:
	-	`sha256:e77765128e74a1290d3c1994ce673a308034c2e97e5b544fa9ff8232da612b3b`  
		Last Modified: Wed, 25 Dec 2024 07:34:01 GMT  
		Size: 7.2 MB (7181955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dfba2a4131c56452a9e76f79338f12d7ed65d04ddddb48e5b17eb1d0ad5fe1b`  
		Last Modified: Wed, 25 Dec 2024 07:34:01 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
