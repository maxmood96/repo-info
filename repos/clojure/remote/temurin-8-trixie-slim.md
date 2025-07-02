## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:42344a88fb6ac955c8bcb4cea457d935101c53a67a4223acbcc6208983d47003
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:71c0b9ada4ff81cf9e37dedc93b8457090cdaf1c407d2d0465eff6726a138e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156289741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c040a7c344cbf7ce90145b033cb19be7c364b87a323777a13de19c48ce302c0a`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71039e295ac88fbe92857fb224fefe5e8b660818f787f7fdf3814a053c6f8d5c`  
		Last Modified: Wed, 02 Jul 2025 04:16:01 GMT  
		Size: 54.7 MB (54716182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdff7602460d7fe35c25b10eb23e6b2a81fdbf780eeadbf53805f3d89422e319`  
		Last Modified: Wed, 02 Jul 2025 04:16:02 GMT  
		Size: 71.8 MB (71811811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33a5e25e4d8e06f06137a8fe789db4278a9ee637824926908f7edfd7c3d6e1e`  
		Last Modified: Wed, 02 Jul 2025 04:16:00 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a6b9d95c6e21d981c15d22fa94bfadb5b37c37f4e630c4cc3252f4a4f7886e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbb63703e21e8d62a3056f1e1cbc47969565db3f01d599234bc2364cea16911`

```dockerfile
```

-	Layers:
	-	`sha256:37dbe7c76926c98b6c57566df8b50a33ab994e42eb82fd730c7a64139a22dc15`  
		Last Modified: Wed, 02 Jul 2025 06:44:16 GMT  
		Size: 5.4 MB (5374412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f719d3443b6398ebd93ca9071e1f0f74b81b79fa671d98bbede6a7da17879d`  
		Last Modified: Wed, 02 Jul 2025 06:44:17 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f6c54ec170ed8337a5c1f237b005c8184a4b0d3f15db49071c2bfa96a3c9bd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155600422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b3aeaf0130febec6d474adf08f03e6fa63761d395d45dbda5b8f0384e5c69b`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3a20bd5bceea4ee71176cb91d690c6a95bcdb6821216fd7371d842c228bac2`  
		Last Modified: Wed, 02 Jul 2025 12:10:13 GMT  
		Size: 53.8 MB (53830506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbeceb048e348d149b108f66d2591000e8cd197edb75782a829966025f25096`  
		Last Modified: Wed, 02 Jul 2025 12:16:15 GMT  
		Size: 71.6 MB (71642408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa926f7d95f54f751796b5a08660d139e639188509de44c91408db5d672c1ce`  
		Last Modified: Wed, 02 Jul 2025 12:16:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32f07cf1d7fc1bc6e7d60357a68e593ecd642f0a4881bd24dcbbf70c17dfc0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5395268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ca98037b9e4836ccd5b2843ec9d08e60ee0ed87037c9a059bbb2d654e5cff9`

```dockerfile
```

-	Layers:
	-	`sha256:1ca6c2feb885414d53671ebe5e3aecf813bfba1c90fad597a92c7c2696e54061`  
		Last Modified: Wed, 02 Jul 2025 15:45:32 GMT  
		Size: 5.4 MB (5380879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa2087abb3089a6c27c73e40ad6a382431d5779e64cb8bee1a61e7ef89512590`  
		Last Modified: Wed, 02 Jul 2025 15:45:33 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:889258ea807ff24a181da6e5b5818efcb46c97ddfde29d607e37242b7025b3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162987555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2099f0b39eda4f951d3e56fefe93db716f7f1391faef90f6fcc93fc53f326737`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9908d4940037b46f055feb2b3656863802b64d465d8e40bf4c8ff383a273f8d`  
		Last Modified: Wed, 02 Jul 2025 09:59:31 GMT  
		Size: 52.2 MB (52167965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62972bcec53e24a99bde44b29eda04b50fb86c72d436207c4f761489ab11abd1`  
		Last Modified: Wed, 02 Jul 2025 10:07:39 GMT  
		Size: 77.2 MB (77232909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6be916228ecf26c71678ab0852f7c944786960d8ddb6b693095400630a67a1d`  
		Last Modified: Wed, 02 Jul 2025 10:07:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7df9819361675877a659c7a2ff54fa0029b2a7db23f06f5dab1cf374bb93e49c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b751ea3341bd0d91b679088bbd1d04b4943f18f806b483a0bb1d0a99b3c208`

```dockerfile
```

-	Layers:
	-	`sha256:70517e3729d99a32470a2ddd8acbda8fff861c1819ef4b658648033630dc0745`  
		Last Modified: Wed, 02 Jul 2025 12:42:53 GMT  
		Size: 5.4 MB (5379376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afbec8218ca3298001c3b5d340b1ad171240eb81f15b8908afabe0cfaa0974b`  
		Last Modified: Wed, 02 Jul 2025 12:42:54 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
