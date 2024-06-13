## `clojure:temurin-22-bookworm-slim`

```console
$ docker pull clojure@sha256:99c8de8cccac678efcbf740343a631d0757f5fb6dcda8e971c19b7c317a2f62e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7a01edaa567f2199af5748f3429831b0cba7eeb9de16a8520b2623d8bbdaee5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254734813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684e90a1a0eacc7147e8ffc251870ee689dbfd7c083ab0a2862c4785bcdd5bad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2062c2f57f845df1d66ee7cb6fb192b0d3afd6913bc500afddca438852906183`  
		Last Modified: Thu, 13 Jun 2024 18:14:17 GMT  
		Size: 156.7 MB (156715514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d1f55b1217f7b4eca81ddafc547b88705adcf23a375187d38e91b5af30069`  
		Last Modified: Thu, 13 Jun 2024 18:14:16 GMT  
		Size: 68.9 MB (68867823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52195ca2ed8a0b8a1364fb148285f88624a957e5b20719535afd917c8c85e9f9`  
		Last Modified: Thu, 13 Jun 2024 18:14:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e67b8058992d1f74fff8f89122250b4980e3252cfee4818607d513c783523e`  
		Last Modified: Thu, 13 Jun 2024 18:14:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:692b70e72b8ae5a4d0b3fee3e3344282aedb3fad1434a036beb5abfeb8349426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4720444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aaa2f92ca82f45e4b09cda8dfedeba8c721ac2a99e08de41849a42c76b13bb`

```dockerfile
```

-	Layers:
	-	`sha256:12961d481bb997ca747acf45daf9706e0ab0fb39c998d5b35930a9d0cdc37a94`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 4.7 MB (4704932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e36a85f6053c86bd5debdab96a2d947d5df5e7f6bf388db18ab93ea71b844f`  
		Last Modified: Thu, 13 Jun 2024 18:14:13 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:53b4a9a8043ed99b91ae9d22b00b7ef548c4ea12ede3563a0188932580ab8dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252539537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0bbeab9827139a0d0ae61e5eadc41fbab9d043c9d2b0bdd7dccb559013647f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d556f73e4c9f57bac26b955ba103d774358439da4efb0b23e476a44efc2c3977`  
		Last Modified: Thu, 13 Jun 2024 12:00:35 GMT  
		Size: 154.7 MB (154738019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e529a5fc30ace21fcc5c078d0a06ab4e01735289c1ee6ed233e5504db10c737`  
		Last Modified: Thu, 13 Jun 2024 12:04:01 GMT  
		Size: 68.6 MB (68620806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777777e585912395d68d8e630605b625fccec4778a78ee1ee3eb0ac422494198`  
		Last Modified: Thu, 13 Jun 2024 12:03:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea98b54c7f6f645c334e1eaaa3dfbd0a826357c6519ee9cedcc0260e8ae6107`  
		Last Modified: Thu, 13 Jun 2024 12:03:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4fdb260cd33ead8f5e729ce62b04814083102a2c24b946330cd301262b56358c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4727370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b7fa45ea4666b6a43a5d06ae298fe02f6990ee112b5c46d43b68114bf8664b`

```dockerfile
```

-	Layers:
	-	`sha256:8e4af04f5f86794b7600ff726812b1adc8dd489c253213b87f24cbb6d20fc47d`  
		Last Modified: Thu, 13 Jun 2024 12:03:59 GMT  
		Size: 4.7 MB (4711317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060b4e760b4d69996107aefa5f2c3763c72f125c44ceae2dcaa5c2839bc418ed`  
		Last Modified: Thu, 13 Jun 2024 12:03:58 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
