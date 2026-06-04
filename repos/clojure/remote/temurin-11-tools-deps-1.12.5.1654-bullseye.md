## `clojure:temurin-11-tools-deps-1.12.5.1654-bullseye`

```console
$ docker pull clojure@sha256:0a1883d514a08f41280f0db67c6ed359e2264f913a801ecb6bb2b55e72bbdfc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.5.1654-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:904afc1afefbbc1b473c66d0afd77806593a5b08d6ab8eaab4575de7967f66cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266167736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f294b377daa55dd21f287f13cff2464a3b1c4c6105ec2b26c4146a1ac7902a1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:44:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:44:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:44:29 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:44:29 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:44:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:44:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:44:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ac62fe0277e6bd8a9358d3e5a87212fb0e4d5f40d42708ddfb61d2e093bf7f`  
		Last Modified: Thu, 04 Jun 2026 17:45:08 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3d43ddf25b75cf77ba63ab6d14e57bd473fc9094529245ee96e478e45fd5ee`  
		Last Modified: Thu, 04 Jun 2026 17:45:06 GMT  
		Size: 66.5 MB (66511974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee78faa2bcdf283111234bffac264c15937323b7bb97614c64c7659b2d05632`  
		Last Modified: Thu, 04 Jun 2026 17:45:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:75ce4cd28eb767bc73bd6847e7bba7d830a1f0de09e298249655dc9077685387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7439324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1be3f03e9e99beb7f77fbc0cb1c2f3ae5f2b19d4dd90cceb9041930ff365015`

```dockerfile
```

-	Layers:
	-	`sha256:4d3a8cf53b0648d89099c1bcb72366f73798eade716efbaec500c6905fb10626`  
		Last Modified: Thu, 04 Jun 2026 17:45:04 GMT  
		Size: 7.4 MB (7424961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe20f731f0782daf04c890d3e778d3c30c2a72f86f3d8b94a718a96a082da2a`  
		Last Modified: Thu, 04 Jun 2026 17:45:03 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1654-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:feef176505f7956a16160130bf9129a4c47d3b9f8a8128fd6a7ac4855febbda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261517223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5873d11706412351ff0894fc063838c4ecee182c3ee74c8bd8d734c0061968`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:44:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:44:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:44:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:44:02 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:44:02 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:44:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:44:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:44:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac026f3af97ec53fbbcdb8031740c5ca0a7abd60076bf5ae64dcbd7d252986ef`  
		Last Modified: Thu, 04 Jun 2026 17:44:38 GMT  
		Size: 142.6 MB (142582230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fbed87594d33e1d0b9a3e656b833380d3f8e63d92479181bde1a7a0bb539e1`  
		Last Modified: Thu, 04 Jun 2026 17:44:37 GMT  
		Size: 66.7 MB (66677771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6c9e331ee26a3376de19f694abde4a25bceac6f6e835a7c762a536c93355c7`  
		Last Modified: Thu, 04 Jun 2026 17:44:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1169c196b1b9920292f6c8b08506af65e4ee4ad291767b4c160ce9ce8d1d6269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7445159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5b2d22892adb056e710d1c9ad3e244652d23bc93f2faa7a9197b8e245bd1b2`

```dockerfile
```

-	Layers:
	-	`sha256:d5efc04c146c056cc2446ab5cb55023a7a8b81c2ceb047ca49143e73db0603e0`  
		Last Modified: Thu, 04 Jun 2026 17:44:34 GMT  
		Size: 7.4 MB (7430678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56eabc3d240efea97228a6e9441a4e53743b18608b4404e86075afe043dde3b9`  
		Last Modified: Thu, 04 Jun 2026 17:44:33 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json
