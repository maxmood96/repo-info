## `clojure:temurin-25-bullseye`

```console
$ docker pull clojure@sha256:f864b1eddbd3b4831ec719915ef905964b69bb99d6f8766ba1032501ca44852f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:25c13f124ce29b2930a9a3eec6cf1d4f24320a9f6ce5c7e04b9a552c7c09d53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215358724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba4babf688693642ceda5bfd4ded1ba58ebea76b00a7d7d1472fda729b5e550`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:40:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:32 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:32 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dec9d6003a9637a40e29c8a3736dbc72d6f6c78f70bb0e65f536b9741d50d6`  
		Last Modified: Thu, 11 Dec 2025 22:41:22 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459cda86103af7cced3a985dcb36f742641a3cd644678f89aa5615016f9e1a47`  
		Last Modified: Thu, 11 Dec 2025 22:41:18 GMT  
		Size: 69.6 MB (69555976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaeed9f2fc8cc69257904992e3a578e8e415f1e055912d6ce267e4debb5e4ad8`  
		Last Modified: Thu, 11 Dec 2025 22:41:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966213908005ed7602ad929f895fe927ad26a83c919d19b2155a16b62256d7f4`  
		Last Modified: Thu, 11 Dec 2025 22:41:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c3d6b3a792c93ea3d654acfe57e1855062026faebb0c40bcb5ff9bc48d748f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09904b15633cd0b6484d2229f1386a3bdea8a79f02dc8b89abd1b2545e16248`

```dockerfile
```

-	Layers:
	-	`sha256:c0de221e5e89acf32cf0745a2c433a2f7517db64ec049fa04baeab83a34237fa`  
		Last Modified: Fri, 12 Dec 2025 01:44:12 GMT  
		Size: 7.3 MB (7347007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f8e80a5a892ff27dd8cd74bf133c98f295ef91a077c1657e6cf692e48c8679a`  
		Last Modified: Fri, 12 Dec 2025 01:44:13 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5ca28109593ecaed7c6703b38ec31130fc50ba8936f4016980d525542d5a1403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212998300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e64c64a73bc393bb411dd0b06a9ae120979593563438820170521228146fde0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:40:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:31 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:31 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2a6690e6c0008900da70fe3c10dfd6c03795f4d60f81e21f3e29f9020fdbc9`  
		Last Modified: Thu, 11 Dec 2025 22:41:19 GMT  
		Size: 91.1 MB (91052502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6f908ecce3cd26289dfbcb682ef01116580092549f6125517bbc722198ba0c`  
		Last Modified: Thu, 11 Dec 2025 22:41:24 GMT  
		Size: 69.7 MB (69687046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843cb7a4ef8ec72c349b50b11ddb68e149e798346899058c4f6202af0b46353`  
		Last Modified: Thu, 11 Dec 2025 22:41:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d213ccec474ca925dba7841662f5e033fa188637ab3389f784e5145d8a4d5c49`  
		Last Modified: Thu, 11 Dec 2025 22:41:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d666dea060ba3fa343cbb0b9606b6591f8c2acbe6ef7d878895ed8f7ab99d859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764c901daaf430ed9780657bca8041550afe61c6a899bd6a3856766f89a86381`

```dockerfile
```

-	Layers:
	-	`sha256:15dc62cafc8453035e74fd93298f0c0f8affa81127b7c806d571cf77f1ae6ce6`  
		Last Modified: Fri, 12 Dec 2025 01:44:21 GMT  
		Size: 7.4 MB (7352127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de1eb11eb39c520f05c8180b39cc77f2c25a15540de29e00ac7da88fc25bd0b3`  
		Last Modified: Fri, 12 Dec 2025 01:44:22 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
