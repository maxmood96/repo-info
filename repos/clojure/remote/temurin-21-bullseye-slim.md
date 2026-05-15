## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:2f6a6ce0b5bac60082ca2e175b19f53d9c85bf579e825438183459080e6c996c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:afdf9ba0a62c6adfa207fcad3bcb0fb5b01c99e44dfe7b0839589dc3d188190e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247616572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf70bbe244eab74663400f79a195abaf973d9a8e99dfa85dfedba5dddbe50a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:15:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:22 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:22 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3048568fdf641fc9ca600abaaf7e6e6c6dc02a3674e24141b42002e162d039`  
		Last Modified: Fri, 15 May 2026 20:16:00 GMT  
		Size: 158.2 MB (158166937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b7df04278ebf4d4fbbe5596a0250e7197ffc792ddd8e62607327e0d9931300`  
		Last Modified: Fri, 15 May 2026 20:15:58 GMT  
		Size: 59.2 MB (59190633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b866eadd1d22ef4235e8e4177f8183c8cb3709124dc8a948091810a10f1c56`  
		Last Modified: Fri, 15 May 2026 20:15:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2825fc176a71c11e1e33764076755d76c746b8d67d1d93841d016a5479b8aa`  
		Last Modified: Fri, 15 May 2026 20:15:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a38da31407059870cfd03022af05ff5af21176cb860f41d33958196a3645a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147c8159bd5056014473086b805e1affe74d78a56e30e93a936b35f4255f285c`

```dockerfile
```

-	Layers:
	-	`sha256:84bdadafbe4b151169f3c7e65eb584b23403ec4fdb1c0c258bd1d5ffe5297f0a`  
		Last Modified: Fri, 15 May 2026 20:15:54 GMT  
		Size: 5.3 MB (5322530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46588f97110a6fe0dcdd119ff909e1cf44322ec4aed7decd8c8ccfd602b6c5bb`  
		Last Modified: Fri, 15 May 2026 20:15:56 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70b4774be74149deb3ae49dba8392084bd7affcd41c1c34c9db6193d6d009e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244564864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f39d306bbb13f1356ab752aa24852aef90114fd8b8ff646e59ccc72ff863fd5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:15:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:23 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:23 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993aebb06f4a6a2fc8a8c24d9bb14af299981b7f4d0cc8558565c16aeec61013`  
		Last Modified: Fri, 15 May 2026 20:16:01 GMT  
		Size: 156.5 MB (156461329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0de2bf131ae31dd64f2638bcfb113f7a3e742d1c9249612f18b2091be298b35`  
		Last Modified: Fri, 15 May 2026 20:15:58 GMT  
		Size: 59.4 MB (59359900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d47672718eb829bf7e7bc76d3c207aa7798e2eae02792bcd2abc1d678261e66`  
		Last Modified: Fri, 15 May 2026 20:15:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37f1bc874809b73189c5f2a8cf9d276c3566d9526dc6654846101b36e94e998`  
		Last Modified: Fri, 15 May 2026 20:15:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cfe30e799e7084bf16ca6d9f4b85c1bd9c338d3eef4b9c628892552e502ce175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5344370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3849a54cae5d22d458946a4748a58adb3c70099e5a7c90a98ef9146d5d2019c`

```dockerfile
```

-	Layers:
	-	`sha256:5abdb92a1a5ba0feba38857090e2a63c982f57fad1d1d7884341e1b65782340b`  
		Last Modified: Fri, 15 May 2026 20:15:56 GMT  
		Size: 5.3 MB (5328262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78af421922d526703fa4eae296ae31af8362bc24a1415333ecf1ed2f2a1f5e66`  
		Last Modified: Fri, 15 May 2026 20:15:55 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
