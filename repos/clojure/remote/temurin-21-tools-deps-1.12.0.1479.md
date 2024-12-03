## `clojure:temurin-21-tools-deps-1.12.0.1479`

```console
$ docker pull clojure@sha256:f1ca76e0fa4bd8100e4a790c9ac4337c75a91709292a4ea69953bad73299b8c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1479` - linux; amd64

```console
$ docker pull clojure@sha256:5f87ad646c2238ed23977563136582e82fb8d44fd265dfa6d7a926f16bc8160c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286810830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fba93d4ce5c91da4ca08c631a0e5c66269fa601e5f451619dfd4aef676fe2d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa67108817ecd74db35b696c24dd97463a4ed21463c8c82af2dd07d386f7b0c`  
		Last Modified: Tue, 03 Dec 2024 03:25:51 GMT  
		Size: 157.6 MB (157568687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fb4e698fbc08374e868ab40f75f459668759b3cd56880345aa6f08c749e8ee`  
		Last Modified: Tue, 03 Dec 2024 03:25:48 GMT  
		Size: 80.7 MB (80743896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b629f1a5aea11e490e64c6c46b551c82ceec56db8537fcac3fca9672c802187b`  
		Last Modified: Tue, 03 Dec 2024 03:25:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5023b770804ec7cc9048b3788c7ca0965028456527975797cb5514e9899c7f`  
		Last Modified: Tue, 03 Dec 2024 03:25:47 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:1675c9b1ffe88daf2050d95675826bce4cfa60443791ea8ca196df777681ad1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11299da3b28fb4e770716bb629ee0708ca2f116b43f2ee95bcc008e46d92e26`

```dockerfile
```

-	Layers:
	-	`sha256:4f2263dca4cb6d459a3b8fbcf3fa2e15a876b86d15802625de9c1a3f39f77a86`  
		Last Modified: Tue, 03 Dec 2024 03:25:47 GMT  
		Size: 7.2 MB (7186282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e478e03632f58ea9ec4c121a885a21a41b58cbee4b9327a2d8c828881c07da`  
		Last Modified: Tue, 03 Dec 2024 03:25:47 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1479` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6e0a87bbe9d826843ec20857c388901a1145105405e64aeeee92fe4c3573a515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286179450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546be9c0b6706e8906a1e378598ccd07d310e5dcd1736cd5ba3df262b1722b4a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2cdaa8d620e3458e01b043a2de8dec93076a8e68d2219825a903a144f593f`  
		Last Modified: Sat, 16 Nov 2024 05:10:03 GMT  
		Size: 155.8 MB (155793069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650009f935aecfe6e7a64d069a2b1126c9a32c37fc319095b838a1c4d17f3632`  
		Last Modified: Sat, 16 Nov 2024 05:42:14 GMT  
		Size: 80.8 MB (80798141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11189ef6d83473d6c9f2ada869fcbd3512329860ff9d47785ca1ba7c36240dd0`  
		Last Modified: Sat, 16 Nov 2024 05:42:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd428a1e3b4b8b8a88dd41b49f703db36af776f7ff49b7c45f6c83a3115d2180`  
		Last Modified: Sat, 16 Nov 2024 05:42:12 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:ea261b865344e9798e397a9b07951f31cdb070a8dab99a17167090ac3b2ba49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15f888465d4a6a2561e8c6535a17475c7a395ed004bacb6b7eab14c788ad12b`

```dockerfile
```

-	Layers:
	-	`sha256:09d6b556b0df936816ee0aaa190addef6aa561be3b26606f42f4eaa7aea282d8`  
		Last Modified: Sat, 16 Nov 2024 05:42:12 GMT  
		Size: 7.2 MB (7193370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ae9f9a6f7cf18802f6491c49045a118838abcca367ddbca002c1b460542e40`  
		Last Modified: Sat, 16 Nov 2024 05:42:12 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
