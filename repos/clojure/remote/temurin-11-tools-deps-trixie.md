## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:22c410973d4622c27712cc4bd4a33541c46a1b4f078a7c1693bedbcaaca6542b
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1d6065bfc41e94933749e4b34c1939efaf90095b9f809f48e741bca548dfb699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279797635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b826b41129c2ae13d4dfed5333594beb37e198a148d1519004ba26ea289a4f4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:51:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:51:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:51:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:51:56 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:51:56 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:52:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:52:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:52:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7fe7508c107f556d889b04406727da9a11a9707d548ffaf6ee52118fdef6ed`  
		Last Modified: Mon, 08 Dec 2025 23:52:51 GMT  
		Size: 145.0 MB (144966600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e627bfdc84110795da03cb050bcc60f3f8005b6f258ab0e2a52918d6f093d9`  
		Last Modified: Mon, 08 Dec 2025 23:52:47 GMT  
		Size: 85.5 MB (85540873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8a2205a8354ff2865d5422e431c3a4a3bc8fe46ad125427a7c4542792817f2`  
		Last Modified: Mon, 08 Dec 2025 23:52:43 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2a0bb39a2057c7bb552502de9f939cdc15c38564beec1c5c2c54477bdcb9ecda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f12b8173409cc6849e99a7c66ce1c7d2f52020cb4f752ee3db20b123f39baff`

```dockerfile
```

-	Layers:
	-	`sha256:7e3819fd63a3777b9db9685575100cf5d499668fd85c350b1e182320a6ff0436`  
		Last Modified: Tue, 09 Dec 2025 04:38:16 GMT  
		Size: 7.5 MB (7487070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89361bcebcbf5ffc1db8a564dac116936bc60013989d1611a00c2bf7bc835f77`  
		Last Modified: Tue, 09 Dec 2025 04:38:16 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08998ff8beb9b2109abbaf1302a6173b8b79c0e09ffa27b65b81def8e1c5218a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276747444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30ca942680e1b8bbffab2911d7438c4cb0d872877e69dec7b42f08a4b505045`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:59:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:59:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:59:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:59:59 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:59:59 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:00:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:00:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:00:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda722c12984ccfc42b9c3ba81b7cf02674ebb532fc4a8095c515e7ea7dd1f15`  
		Last Modified: Tue, 09 Dec 2025 00:00:43 GMT  
		Size: 141.7 MB (141731577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f1c01a8d82d9fb9b86d5f082393240f5a5447e90ec57c391194fb5d74af38e`  
		Last Modified: Tue, 09 Dec 2025 00:00:56 GMT  
		Size: 85.4 MB (85364997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b1850314252167b2bc462d925f3b667ae108cb29bd20227d4903ff8e8b3862`  
		Last Modified: Tue, 09 Dec 2025 00:00:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a099622df435a19a7066b77f472bb69d5444e7b932117f242cdf5e956818cf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7829e9b76a1b93495cc7c90f00ca38fc31ca21fb7fbf1000d53dedcc6531b62e`

```dockerfile
```

-	Layers:
	-	`sha256:1f6f1cd47bbb831113e5a394f7aa499b94894321997bfea58a357f51869115a5`  
		Last Modified: Tue, 09 Dec 2025 04:38:23 GMT  
		Size: 7.5 MB (7494718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb05846fa02be9126218f8a40e2565eda5fe1a9bd54841fa89687a9e8ff1d8fc`  
		Last Modified: Tue, 09 Dec 2025 04:38:23 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:4e8fea3d07d3a25b894d79cb4d86e703807d882bae48ccac4e424f0c54fa3cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276138403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bac21e3cae22f0936a8a5686321f300eee3c5b404746e8d9059fd0beb0b007`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:25:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:25:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:25:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:25:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:25:26 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:26:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:26:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:26:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37d1cc451357decc266df875d9334bbd4504581a335e8cd24c32ce8844bcd57`  
		Last Modified: Mon, 08 Dec 2025 23:26:56 GMT  
		Size: 132.1 MB (132081948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604dcd346da19afb81c32af5f3b9feda81de29c4f03371dc8ef71d9531ade219`  
		Last Modified: Mon, 08 Dec 2025 23:27:19 GMT  
		Size: 90.9 MB (90947332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058fea3ccdb73aaf3a9550fbe04f41703f8156fbdf1dcb8965ab9572129801ef`  
		Last Modified: Mon, 08 Dec 2025 23:27:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:25c954d1212362623235bd7f746568410731d9e08730712893483d3090cf476c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fd1ad5565ca9acc1babd57e0d376c94710306030282db8f103eccfccc5a477`

```dockerfile
```

-	Layers:
	-	`sha256:fc94fb298c13af2b02908ff6f70354efd9d5122b0abc6603ddd70ff4ea70417f`  
		Last Modified: Tue, 09 Dec 2025 01:36:07 GMT  
		Size: 7.5 MB (7490874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ecb5f686385a1f59f6cce1d8448c4b690fad8242aeab3065d799fc63e6e02f1`  
		Last Modified: Tue, 09 Dec 2025 01:36:08 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ddf1a67df7f41dc2e962eb5562ffce3e48018aa33f428394be26ffe54411932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261552294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8d2edfb539dee953578bf7da218f095582c94aed6f9f391fa47816d54dc3b6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:26:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:26:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:26:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:26:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:26:21 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:27:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:27:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:27:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc69ed7ad4f3a48490b63f8e4fcf5d54f88806dc48f2b192a8299dfc58163b`  
		Last Modified: Tue, 09 Dec 2025 01:27:18 GMT  
		Size: 125.7 MB (125694401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791e8df89be684baffda988156b325358aeb410620b6bf35ec72ad1ff3e56189`  
		Last Modified: Tue, 09 Dec 2025 01:28:27 GMT  
		Size: 86.5 MB (86511340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c33261e57300c32aa66241229458dfda8ae2dc1b27b37bc878f143434adb7b`  
		Last Modified: Tue, 09 Dec 2025 01:28:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b24e4cf89d2a16aa09311420afc41cdda2f0d41fca63f930a8a86a454cc0bec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59ad9a0f5ccaa5d7c6d98d1d0309a9ef93095f6489a572c976dc78e85a410f1`

```dockerfile
```

-	Layers:
	-	`sha256:efd159770c4c8133b2a60ed1cdf695b1bc8fcaf5aaf7273b3ee7c4451787b43c`  
		Last Modified: Tue, 09 Dec 2025 04:38:50 GMT  
		Size: 7.5 MB (7482996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd25d57b4b533fb5aa72603e3efb2bbbf1a1a6503b59816025067a17a625d659`  
		Last Modified: Tue, 09 Dec 2025 04:38:51 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
