## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:56914863e39a4f53c7642b1bf22083006d53d42a2307861a5292d24c2bc9334a
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
$ docker pull clojure@sha256:ecf1023767d2333f5c6d4413ca7652b64190df93819d58031f498bf822a033f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 MB (279357807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b90d260e2b42aad49757ce8d6a777ea41413c960bdc1413c74eaec4f627ea3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe444f6a2fe58239848b2116f35954a224103bd19a3916c50b284a83450c230`  
		Last Modified: Thu, 14 Aug 2025 03:16:51 GMT  
		Size: 144.7 MB (144693263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd82cbf40632d1b495fdcb6e5f2c4d76b244233c5bbd3429a424ef425af1eb0b`  
		Last Modified: Tue, 12 Aug 2025 21:37:05 GMT  
		Size: 85.4 MB (85385226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14e269f358703f3752d3a9fc209d78d23262fde774b134e8827417236fe9cb2`  
		Last Modified: Tue, 12 Aug 2025 21:37:00 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e26129ac0a010f4a9a0b57bbb60a5cce770ab0c80c6e8e9243fc15e0a4fb4`  
		Last Modified: Tue, 12 Aug 2025 21:36:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:87b35469de8425d9b36192afb929f661d5b0fb2f73265e0ca2a95101e87c1fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7477989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af37565f133375cc9ec45c8b62ad129b0489f05857c7cf750c1f84374b061d63`

```dockerfile
```

-	Layers:
	-	`sha256:848d2860ee837ed998b4ee6db2d0e7cf3e39406ec7a05c884ee6df41bf110b48`  
		Last Modified: Wed, 13 Aug 2025 00:37:57 GMT  
		Size: 7.5 MB (7462192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61aaaefcbd09a04a315b92e08efbc91e45fa5f54e4c237ade9db716c104c8f2d`  
		Last Modified: Wed, 13 Aug 2025 00:37:58 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ef3c6ab9399672c06cc7ac30f2d0cb4216d2fff375ecaf2f543dfd76c2ddda62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278395590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb35cbd1d015198e6b8feaf549a73431ca6ab0948b63463a1b4698c18f95ebd7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc0c23a61ebb55d12d9b26a1da48db98dbd08ff68a83d21764204345eca2e72`  
		Last Modified: Wed, 13 Aug 2025 14:24:22 GMT  
		Size: 143.5 MB (143542130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b95de0a728622ab1b80ae036100f09f8df6f725cde578dd77a00924f95304e`  
		Last Modified: Wed, 13 Aug 2025 14:28:50 GMT  
		Size: 85.2 MB (85210814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05379c106b366c1d05b22f42f5e8b7c3e24d6f4854869fdaedf0dbcb22b26a26`  
		Last Modified: Wed, 13 Aug 2025 14:34:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22d5ea2d48eaf4ef4f5c183530c854d2ae3b01fd861017a3bfe3250d4425f5b`  
		Last Modified: Wed, 13 Aug 2025 14:34:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c15d1ab3917bf0508f068946d9c33f972b73417f2ca38d7ef7d09892ebb636c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5534d81b9d6ba4dac71ae58e96162bbbbc900fa0d96a5477ce93507506bd16`

```dockerfile
```

-	Layers:
	-	`sha256:7f56b1a160e0f1f20b8b87c4eb05688cdac6a8fd67c9ae1819d44a565613e1d9`  
		Last Modified: Wed, 13 Aug 2025 15:38:18 GMT  
		Size: 7.5 MB (7469222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2622d4ad693817912187082c5448b21f359cea4b9c2a1cf4dd7368bb81464f88`  
		Last Modified: Wed, 13 Aug 2025 15:38:19 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8fe3c8b6c64f59ce634cd1a1f90e59173b42488be3095ca15448930c5450d686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288271950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7dd019611852736cc7f28d2eb5f5bb993f128a0d307c37794b919c9aca11c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4684e1ddb8b97a1bda15b3f19b6ab48e42f3d58f66a7c06292b36dd776b301df`  
		Last Modified: Wed, 13 Aug 2025 19:51:06 GMT  
		Size: 144.4 MB (144372853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981c65923cfcd969d225329a163859a2f4b1d3ff9c2feb949d2a0105a81ca5ac`  
		Last Modified: Wed, 13 Aug 2025 19:58:34 GMT  
		Size: 90.8 MB (90794673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25555137e00b1ec284b891fd7e87aa6fabeac279f1ed409a65dffe46192440c`  
		Last Modified: Wed, 13 Aug 2025 20:33:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605941d96c32c823d9a07ea3b978a4eb2b3f267eb1f8a63f97160e753ce1165c`  
		Last Modified: Wed, 13 Aug 2025 20:33:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bbab94c8709f62edeb6b7211519ca2595b9ee0f756d2628ed7e0b3f53a015e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c81ed17ed0639320c001fec5b097b709235020334fa45a8d7ae1bd0dda75732`

```dockerfile
```

-	Layers:
	-	`sha256:960fa04a464a0c93a0f9c49550b31468fd3e5dea175c3a7fba2e42d2d4ade4eb`  
		Last Modified: Wed, 13 Aug 2025 21:37:29 GMT  
		Size: 7.5 MB (7466611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3213973b06f29411103282b3a2beca16fc2a29a8bf3cb849249be925f06c97a`  
		Last Modified: Wed, 13 Aug 2025 21:37:30 GMT  
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
		Last Modified: Fri, 15 Aug 2025 07:07:32 GMT  
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
$ docker pull clojure@sha256:77f101d55ba5181864a812d9390631b99ff244f102c1ec8d40d42c9a544e3ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270424559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7590acbdd5d34cb9ece10a9ab22cb92b79b562d0c4d781ced1760608189d365e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e0ed6f599d127798680289c0d3e681982f0ec78b9ef2a0f817dbc95d09d1c5`  
		Last Modified: Wed, 13 Aug 2025 07:13:45 GMT  
		Size: 134.7 MB (134724419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96bfcfb15c3fc25b828066463350817a4a5a86ca6f74736413461d057a6f292`  
		Last Modified: Wed, 13 Aug 2025 07:18:44 GMT  
		Size: 86.4 MB (86353934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cc00bbb740260c021251eafedb3c0959a25de5ef5b9d3c23394bacf62e00b1`  
		Last Modified: Wed, 13 Aug 2025 07:18:40 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b683a21c3408000af83dca828b5c6761ede68f036c82438c785960887017d9ec`  
		Last Modified: Wed, 13 Aug 2025 07:18:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:668efa122946efd379032308421fe1a1b50768c26e21ccde911a24bacb49c024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1296bcd47e5a38260a30128bccb832e3575115f29d6d075039371ece57ef30b`

```dockerfile
```

-	Layers:
	-	`sha256:46547674044fce68aa9a0e9a71c22d688ec81f904cbc4afb69b0bc70eafc5dbe`  
		Last Modified: Wed, 13 Aug 2025 09:36:59 GMT  
		Size: 7.5 MB (7458114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570c248946c887079cf4314c47b1bb96ddae7495f511437ebcf50a4c7b4ec8ed`  
		Last Modified: Wed, 13 Aug 2025 09:37:00 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json
