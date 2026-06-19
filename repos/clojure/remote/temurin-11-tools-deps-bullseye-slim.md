## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:84c52a4f1cff6cb45f1f5ccf8ecfd1885c396f06b0d09d62e39472962ac65703
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b4aaa6e049f5f3120b5e44a74c2605bfa0d8d2da369272dd7fb1e58304d36c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232247325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855fa316a839972fa60dcfc8bc43bc297159b92fd2defbe050ab77999cfbe091`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:13:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:13:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:13:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:13:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:16:28 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc937bfd2d2beee3451e7021bcae9f7d70d9fed3d7e19e274626b2651b59f57`  
		Last Modified: Fri, 19 Jun 2026 02:14:22 GMT  
		Size: 145.9 MB (145886162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc5b94e6f574ce657129d893370d7ce2800faf0365787660df694873cf4f829`  
		Last Modified: Fri, 19 Jun 2026 02:16:57 GMT  
		Size: 56.1 MB (56100263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf02fd33a4f530ae22886ebac1ac3fcb85b5769504d0706cae6ba07328ec73a`  
		Last Modified: Fri, 19 Jun 2026 02:16:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:255b2e545637100ae04709851e5afedd9e429e3eda0aed8c4781c38a88448ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5353410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0a0bbe2d07ed9d71fea978076d3cd43e56315056fb49a982b669f3126f038`

```dockerfile
```

-	Layers:
	-	`sha256:8292abc4e26dbbfbf8997d6277026539c843ac9f3d5bfc9960afdd7ec82fd5f0`  
		Last Modified: Fri, 19 Jun 2026 02:16:55 GMT  
		Size: 5.3 MB (5338989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccebb4aa1b9b914dbd4e9594ad60d0cf3ee7197554a6b16190ef6b3f539c4057`  
		Last Modified: Fri, 19 Jun 2026 02:16:55 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:88902e156b2860fb2d09bf7fb495ecaa00dd7bcc5822a3d47e697a8d731cd4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227596443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7eaffd5a484f720767ec66f506d45d84b844303db2810174c4e526274a430a9`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:16:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:35 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:16:35 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e82b80aa9866de460eaef9325952f991bf861a3e07e9395772562875a0160f`  
		Last Modified: Fri, 19 Jun 2026 02:17:11 GMT  
		Size: 142.6 MB (142582160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06036c4a024b66604bf7149795fcc54b37f6725123d1c23b93c95fb75459381`  
		Last Modified: Fri, 19 Jun 2026 02:17:09 GMT  
		Size: 56.3 MB (56267488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63eea0c13ca2ed7fcc01e69cfab82f58f5938db0bb75b003bce727ab8dc329a`  
		Last Modified: Fri, 19 Jun 2026 02:17:06 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d40b39342412a4e343f3e1953000ee65e3ab98fab02e4138114ddb9183db7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5359878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c08a516b8beaa71453a70135c7b4efacc607b788479084cdf6f38b06b14d188`

```dockerfile
```

-	Layers:
	-	`sha256:126980dedc89408a9980756ca405e01c884b113e6f76cb74fe9c7143dd2174f4`  
		Last Modified: Fri, 19 Jun 2026 02:17:07 GMT  
		Size: 5.3 MB (5345339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2051674921a18c08e961462f237dc939218fa27a24936a071a801ef4c248daaa`  
		Last Modified: Fri, 19 Jun 2026 02:17:06 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json
