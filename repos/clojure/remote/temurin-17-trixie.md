## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:76a02850eb83886eb59647f611438f4e15e5106e08a335c22a82da9ba6698464
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:981af1bfbf2dc6208a46954efbf83c4e3a759d72a150545607b4b7c8c19424e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 MB (279408002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1eaeb7d409df002c951a6dcbbceea805b55cddd735e7e0a019041b182f73c3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efa4a112a2078c37c5f5c8e62716fb1abc95fd266a10def30fa32d785e1a196`  
		Last Modified: Tue, 19 Aug 2025 03:41:16 GMT  
		Size: 144.7 MB (144693296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d58e09d2c5370f82c5d6b96fa3e114c12e38afffbbfb86dca5c6a73a9da5e`  
		Last Modified: Mon, 18 Aug 2025 16:53:15 GMT  
		Size: 85.4 MB (85435385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1827930be88d0963b7d7e2cd62d3d556592154c8baafcf0de6f9ab7a8bbc03b5`  
		Last Modified: Mon, 18 Aug 2025 16:53:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2b024c5da530d064fc12f7f63ff7274f27aee3da6cf34e2cbc8969abc9483b`  
		Last Modified: Mon, 18 Aug 2025 16:53:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:527855f3fae822134df149ef6eb827758b7c8bb56df0a6dbff8d0b8296039ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7f0828312a3a6cc2f8e6471816f2ca13430ff226ead32013b960c4b97eca03`

```dockerfile
```

-	Layers:
	-	`sha256:9c36e648c91ccc4fce44bc6c1d605b4f8fb412d5a58a09754e8ee8a758a39b3f`  
		Last Modified: Mon, 18 Aug 2025 18:38:56 GMT  
		Size: 7.5 MB (7462221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e7f9a567f2b1ce28d48ddcf3d182cb23b233aedfdddb99d5ef9986b0fc7516`  
		Last Modified: Mon, 18 Aug 2025 18:38:57 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4e2002dbd1fb4a4949b5df24f5b0f076b97b5a9d7a255b86bb93ebaaf2bf1a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278440719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df750b51cc4e6d4b1f6e835b00af44befa6fa1025f46ddb7f8bb172d77357ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1b4924db0e9a6507273f53942c071f009dd0878c2430f6b5b0b67f21e1720a`  
		Last Modified: Tue, 19 Aug 2025 03:42:04 GMT  
		Size: 143.5 MB (143542131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada9f2ed383c136f12df983f0ee89d133dbd78f92a88a858ff4f088da76668b0`  
		Last Modified: Tue, 19 Aug 2025 03:42:03 GMT  
		Size: 85.3 MB (85255943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae317d16fee19f462cda3143b0d260e2358b86b872329cc3b2b5801d2dee33d`  
		Last Modified: Mon, 18 Aug 2025 17:11:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fb4d235a21fd858c469909e0601404815a0780de5017b121f4af16a4b40e7e`  
		Last Modified: Mon, 18 Aug 2025 17:11:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ed41679ad47a2694d78d316bd953c4974df63a58781cd3f1d5997440f46d14fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77fd9727228700b121da07d6e0bca7c430d192b411a91ad8d89d19b6a26b166`

```dockerfile
```

-	Layers:
	-	`sha256:8cec0697ce8e30d1bfb122aa502303ebe8d2554969140576bf6826aa8b584c84`  
		Last Modified: Mon, 18 Aug 2025 18:39:05 GMT  
		Size: 7.5 MB (7469251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a56cedcc8dbdb1e1892be091099522db962fe03fb8927dbb3f0a1689009ad895`  
		Last Modified: Mon, 18 Aug 2025 18:39:06 GMT  
		Size: 15.9 KB (15914 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c674b42a3634d8f13aba006a18c27576a0c6324339093230b941acbaec117bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288317742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb97143d6d0c2cb6c14b42114c9c69145da031a22403cd5b21caaa2241fe0f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5096f4531428918861fb2e9c0966a5ff7b6e852e32764913f3a77fdb5d16a0d6`  
		Last Modified: Mon, 18 Aug 2025 17:22:29 GMT  
		Size: 144.4 MB (144372854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae99f57bc5a8305f0f80e195de4faa5c24d086ed1d043ee904d0ec0b263063b6`  
		Last Modified: Mon, 18 Aug 2025 17:22:59 GMT  
		Size: 90.8 MB (90840460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0829e65eeefd7d937d1446ad0010f7e010f0984288fd889923cc6a941abe33dd`  
		Last Modified: Mon, 18 Aug 2025 17:22:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6740b6f8a7ec7749564cdbb46b8b6f454f6e9c375c439e1b8443977f4087b46`  
		Last Modified: Mon, 18 Aug 2025 17:22:45 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:89eae2f8a4bf0ed9118791be8d256eac9edaadcde9ed20cd60939e478bad7978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58fcebf786186e9188717f2215c89048711827a370ef4e2849606dda291a8813`

```dockerfile
```

-	Layers:
	-	`sha256:94c0d0b43ff6a7eedddc5417e6e69e26f753230a0b7bac5994ee7d2d020226cc`  
		Last Modified: Mon, 18 Aug 2025 18:39:13 GMT  
		Size: 7.5 MB (7466640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edb6e31aeabfdbbeeb9902c99bdcc04cc97c508b7772f29655b254d645d2b26c`  
		Last Modified: Mon, 18 Aug 2025 18:39:15 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:184c290f2c58711d403e29f9414149b51f5c6515db3e662d06bf77c516c32a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270616988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c96ce557336062c0934a7455376e7f8bb916f6ba5822002418422931889053b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a928c7cdfc198fcf48e44ac3d7ec40b68f0c9d3a829837b5eaa4ea421c0a0de`  
		Last Modified: Fri, 15 Aug 2025 17:54:57 GMT  
		Size: 138.6 MB (138575687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a445ce7012cd51308b46d91518e6f1717107e2f60991f475974bf23fe46251e6`  
		Last Modified: Fri, 15 Aug 2025 07:23:38 GMT  
		Size: 84.3 MB (84275956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41bbcc835ce27247a3cbf46353bdd88d11f559123f4879979aa5d89135dc1c4`  
		Last Modified: Fri, 15 Aug 2025 07:23:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13a176905962bcd4cf8e4323a93ef1def4ae80c6f54a8180d134ae3c14b15c4`  
		Last Modified: Fri, 15 Aug 2025 07:23:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:303377ecc9535ad52b6fc2689a064e0fbc03588a0f4dcc6b9926ce2431489314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7464031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d33c4998ade189d914da92d5a1623e9dc29439591a0a87aac2223876e4f347`

```dockerfile
```

-	Layers:
	-	`sha256:5be424747890a515754db0871a55fa4492894beae008107e77eb53fcef1b657b`  
		Last Modified: Fri, 15 Aug 2025 09:36:02 GMT  
		Size: 7.4 MB (7448186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36142563b87a50f4b0103d008d8c880b0168e05ab5d7bf92da0df429e473bde4`  
		Last Modified: Fri, 15 Aug 2025 09:36:03 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:656dba6e6b330acae757dd7384b9459d9fb15083079826457eefb6fc95949ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270473929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fea1a3f5000ed7c1a0cd0524852070d55108a193dfa7bbb9e6451ed9bfea59`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ef58001aee7acf83166d5ef416f4116fc450dc5d1056018e93ccc35ce853d4`  
		Last Modified: Mon, 18 Aug 2025 17:43:57 GMT  
		Size: 134.7 MB (134724432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4ced70cca78a2f20114e2d49e2d95e2703783383ee627aef814de94e2a97b7`  
		Last Modified: Mon, 18 Aug 2025 17:44:13 GMT  
		Size: 86.4 MB (86403290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30fd8c436f06876e830d3cb3f24d1870d1b36a7a90fe1260c9765f269b67242`  
		Last Modified: Mon, 18 Aug 2025 17:44:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778b2f514d92a0b05fbee00fbbe3762c49388466809d50b034044c3dcda9857b`  
		Last Modified: Mon, 18 Aug 2025 17:44:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f3e1b394204f6d29e318d1fb55bd05454e29ec1d6ec893bb94105f6344c0b756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39655b6f7e2e5305628ae0a77744fbfdfa37bc27daa83ba33c69e5d1e2db1fd`

```dockerfile
```

-	Layers:
	-	`sha256:1b6e0f7362c514bf61924128c65a1bb40d972258ecf2653bc5ea5b81a1d01d8e`  
		Last Modified: Mon, 18 Aug 2025 18:39:22 GMT  
		Size: 7.5 MB (7458143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8350fe102acbfbd0dfa0e25f4b8b854d48e32ed195be3ffa8df5dcb2d688afe6`  
		Last Modified: Mon, 18 Aug 2025 18:39:23 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
