## `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim`

```console
$ docker pull clojure@sha256:7be192b76272de5cf6e90cc79c07635965490d23e97d2b5d55b5083d35bcad98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a5eddb7ccf8ce23c2f12bdf7e0605f8dc800a0f2b5dfd6d6bd83b846a33b627b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150079677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2880129af9af7012eb6f634f8f7311bf5c026ccb084d6aece568a0a40f50bee`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:14:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:14:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:14:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:14:42 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:14:42 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:14:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:14:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:14:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141e6faf845c83c92d2c014978828fa729300ceb06e3bad1e37ea6bcc9e3bbba`  
		Last Modified: Fri, 19 Jun 2026 02:15:11 GMT  
		Size: 55.2 MB (55198705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e71b60cb798915ef754d9f44d328b8cf6fbff80531a233b40ca7927187506c7`  
		Last Modified: Fri, 19 Jun 2026 02:15:12 GMT  
		Size: 66.6 MB (66642704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9ff5a3a3f2aec9de2ec6b8acf6aa5e822b00ac7a0bbdb83adcd4881c96806f`  
		Last Modified: Fri, 19 Jun 2026 02:15:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af77ed60fb6b0fa6dd1252a99f8b19c48956aaa9c9462048f1130d80b5026077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116a56ac987e2039f720fb8323451f9f26567134ad7f14262a188f73a7ffb492`

```dockerfile
```

-	Layers:
	-	`sha256:2cb0594924d48dcdbe69d09e2bbacc6985841a1a31e6b157204ed3daa4cbad87`  
		Last Modified: Fri, 19 Jun 2026 02:15:09 GMT  
		Size: 5.2 MB (5234359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a47d85026972b408f36d42edca7cac4d652d903affe1d5d7d0989c0d07ff08b`  
		Last Modified: Fri, 19 Jun 2026 02:15:09 GMT  
		Size: 14.4 KB (14402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dbfe954e566a0f0e1e68b1a9884eef72f1c090728b0bd8e3010939f0d87c1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149038828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94297af935e54000c4c2125fe0885a12b7d22984c91d6949ac1d3389d734db2d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:14:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:14:50 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:14:50 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:15:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:15:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5695eab9255785db99a025ab33629abf114e030dfaadebd7caa4ba5009b3f3b`  
		Last Modified: Fri, 19 Jun 2026 02:15:22 GMT  
		Size: 54.3 MB (54272921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1db1075d01bd0d5f3fc4fb247c69a302e27dbc802940075bde6508df7d58d`  
		Last Modified: Fri, 19 Jun 2026 02:15:22 GMT  
		Size: 66.6 MB (66642955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e611b63dedc927bf7600a5c5c462ac409bd862fdb767f8aa9db305ba2219a4`  
		Last Modified: Fri, 19 Jun 2026 02:15:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:40398b3be6586e2984473df18f6f0e08a00355f4409d72bddbbc418d757742af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11d1946e43e80365e04527a8b9f042e98e0e154858fc9e664add1229fc871c3`

```dockerfile
```

-	Layers:
	-	`sha256:052a08d265ef1ab181700a3675065d986f5833bb1d29e53cc9129f1dd1de7e7f`  
		Last Modified: Fri, 19 Jun 2026 02:15:19 GMT  
		Size: 5.2 MB (5240820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f648a75b5f8fe4a7b1f66858bf144be97dde78840586214e1c393b3f0f2ecaa`  
		Last Modified: Fri, 19 Jun 2026 02:15:19 GMT  
		Size: 14.5 KB (14519 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fa720c50dc9d39330c20a4e4459a16cfc600fa68451b971da33fc6f0589301e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157227865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29583d66ca42f4b4489e5ffe547c5b8858d9d73fdeaef715cdf80683ce6b7a11`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:21:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:21 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:21:21 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b907d7417180342b0cf27708e33be1026b729e843c213f71aaf9b477ae2b8ce6`  
		Last Modified: Fri, 19 Jun 2026 02:22:46 GMT  
		Size: 52.7 MB (52669121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173b28ad8dc3254e4272dd73c01f7b2af438a35e08073da3fa0b26f593f1d872`  
		Last Modified: Fri, 19 Jun 2026 02:22:46 GMT  
		Size: 72.5 MB (72476158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aff38e3f6b0cb51ef8e06c370645444038202b52b922f0d1f41d83ed9f83e0`  
		Last Modified: Fri, 19 Jun 2026 02:22:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dcabea9b9a4fa59ac2b7308cca102cdcabfa212bb97a889887a87910a0e58959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003cc742d3ceefaa061a08524148cd2d7fd8c7a9fac2c53d76abe1495c4342c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f7c6eece09ec2163e50dd388742f3947bf2d0915be0c921824741fa3d5d9151`  
		Last Modified: Fri, 19 Jun 2026 02:22:44 GMT  
		Size: 5.2 MB (5240112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5c313053141bab478a14701f68d95e00a1d60c0ebae5a89fb73a3051b7d1bf`  
		Last Modified: Fri, 19 Jun 2026 02:22:43 GMT  
		Size: 14.4 KB (14449 bytes)  
		MIME: application/vnd.in-toto+json
