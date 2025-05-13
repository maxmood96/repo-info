## `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim`

```console
$ docker pull clojure@sha256:f39c2a2210b006ce6425b581dd495b254e975516a707a84512064ea9c52dd94f
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

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:daa953f5ba697b93a383213af841e1e7367fbffc7265d2cb591f595419518cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191430988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4503ce2d6ea51c154df3ce013c62effa542c077d07e079d46438fd4fc75ddb10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ae34fc80ed56f2b3a9a0b682b58e28e57fe981f5e514c3f687044f4b967608f`  
		Last Modified: Mon, 28 Apr 2025 21:08:25 GMT  
		Size: 29.8 MB (29753912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543a4cc9777670296712f6a9872398e4d4ea99fbbc7cd6c8fc0c4b43902d72ce`  
		Last Modified: Tue, 13 May 2025 17:53:57 GMT  
		Size: 90.0 MB (89952000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee2cb3f7f9d8ca4965002f2b869a674e825f883763d550bc2f0f5ec0d40a6cc`  
		Last Modified: Tue, 13 May 2025 17:53:58 GMT  
		Size: 71.7 MB (71724037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81f8a5667643cd7ea85b65caff56ee1803a9ab0df3ec8eabf041e825b2f5c2a`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd344e9802cca5f089023d85ee1628a25d18e6803d73acd7efc8e4b6530a6c6c`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02c7857900867b63b57dc20a6a2807e68a95b113ba63482b3209825449316689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5033181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59433a590b2b0d5c6d9997077cb57f13c9057d161c6406da5c21a5132fdaeba`

```dockerfile
```

-	Layers:
	-	`sha256:098d006171614f80d837a7b2cf6084cf0491aadeef5f6edde624611f10d57e57`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 5.0 MB (5017333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b2a218b63474ed7f5e09aa661da929ad97a99046dc626c9f6131b904f91de1f`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bc452bdfffec80a52570be4c3fc9f1066703d507a20a5e5579fcef6929120d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190868809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e6c0133162ff11b2f528d7e50afe0dbe0daa431813c956c8657d6c59897cf9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Mon, 28 Apr 2025 21:23:36 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf78d6205bb385dbaea21715ebe2773e6352d0ca5870bdfcb0e246524d354c9f`  
		Last Modified: Tue, 13 May 2025 18:09:24 GMT  
		Size: 89.1 MB (89091185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b82f5ff77071957a46ad0bbf072d8fc45c22d89872e04cf749ee5345d7cf2b1`  
		Last Modified: Tue, 13 May 2025 18:11:31 GMT  
		Size: 71.6 MB (71646356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c528f3ac11805a1dd5769746be59e1b69c1fd644e634814b8d88cddbb1703eb`  
		Last Modified: Tue, 13 May 2025 18:11:28 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e8b0e9b65ab1ef53701ec31c7eebf3b364fb8884a2a65eb51070734fb44ee5`  
		Last Modified: Tue, 13 May 2025 18:11:28 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:741f432648c64ea962929480e17378fc938b9abc9ce2c51405cf47d6b4231520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5039064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c326b0ef865df419347b5770ede22b21820c79504cefed3e6ccc951be95acb4c`

```dockerfile
```

-	Layers:
	-	`sha256:5cef5ffdb4fe16bfa3603415d9d145d19b7600ba1eac195c9074876e8fbedd8c`  
		Last Modified: Tue, 13 May 2025 18:11:29 GMT  
		Size: 5.0 MB (5023099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e001abd2d850fda1f5eb776b9e9280d05702ddbafdd7d17b0542f055848c4c`  
		Last Modified: Tue, 13 May 2025 18:11:28 GMT  
		Size: 16.0 KB (15965 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:aceae28d1603d12c8921d26488000f90876b08959fc0e89060eb2ab80a9a763b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200713883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc7cf8b579390766f0fdf8267eda12c3078d2066e5ba866584c768103045d32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a739447e8599431e1e4996b4b6d4022822d37eddea9a3737acbea74b8a860d49`  
		Last Modified: Mon, 28 Apr 2025 21:25:59 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8803762d089e91a891a211912215216c857d1bcb4d597780a3b0fa903fd22f`  
		Last Modified: Tue, 13 May 2025 19:37:16 GMT  
		Size: 89.9 MB (89920243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63235b607e1043b74347ac88b0f5477c1605cb3399008f758cc834da7660e04`  
		Last Modified: Tue, 13 May 2025 19:44:30 GMT  
		Size: 77.2 MB (77214905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3593b4b9cb9b0483c1c1b7f90fe2a9e0b8a28f30da5af364396dc4abd3772369`  
		Last Modified: Tue, 13 May 2025 19:44:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c58210d21e481a0649dfa5997f4576302d8513ff3a2deb618f94e63fc0ff196`  
		Last Modified: Tue, 13 May 2025 19:44:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3b33cc89830032075f7614a74e5fbed453fec82dbfd76b53d8e4b0e1b3411a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5038736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37d83c88c03f5c480961c867a878345bfca19540de9e2577d51c77e8a77dfb`

```dockerfile
```

-	Layers:
	-	`sha256:d03736efe85864671424e4034085fa38d957f0ed378390bc2a9af55269b2dc2f`  
		Last Modified: Tue, 13 May 2025 19:44:28 GMT  
		Size: 5.0 MB (5022840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5287ca572e65bdc081bd0e16cc451f1a5a426425a86a3a48c2e531d40d084cee`  
		Last Modified: Tue, 13 May 2025 19:44:27 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:2bf1dc55805313c88a90140286a5be7050d3c794a1f0b2437f37c3df26ab86e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186566791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd9e594e9751c65c01fb1dc7160165b975a5cf0aaeb2062e3b7352f41174d97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:facf81ceeaa2f81a0f9ef1ab66d52f94aba08977754588b2609aaf3106342525`  
		Last Modified: Mon, 28 Apr 2025 21:17:50 GMT  
		Size: 28.3 MB (28251718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8546dd41fc9c11a25a2d3b37db7dd48c5347012a22efde93115ea1f1714c8e`  
		Last Modified: Tue, 13 May 2025 19:42:38 GMT  
		Size: 87.6 MB (87622251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d403c4710f04a898f180a8fa7e18e3407cb60d791eac38bbac6d669e76959c0c`  
		Last Modified: Tue, 13 May 2025 20:04:37 GMT  
		Size: 70.7 MB (70691782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1ed6212e0bd2d92dab9481653cca0ebe843eaf33dcc4fdff8f56452a02517`  
		Last Modified: Tue, 13 May 2025 20:04:27 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819f4d9a13d3e06ddda0edc40e0c3b03364a6e9d62b1fdb2ba0fb8755ad48ae8`  
		Last Modified: Tue, 13 May 2025 20:04:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d0353ea7865dfa78896c2fb5c1b3a0039905ad2bd9f706f87b5a64af1ef4eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5022808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1b19c807026d217dc366f80acab234283d20319d9281fd1a4fb62b0de177d1`

```dockerfile
```

-	Layers:
	-	`sha256:e6fff4bf5338ac48dbd37afb543a67b027c63bea8674af12cdacca362d6e1e5a`  
		Last Modified: Tue, 13 May 2025 20:04:28 GMT  
		Size: 5.0 MB (5006912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd6edd682a1e6d8cf9e6d8f4250e48a8e23ec630703c289ab1d3fb4ac92df4b`  
		Last Modified: Tue, 13 May 2025 20:04:27 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:96f86ae0df5b9ea83e0be0668d1e0f5a97ee3feafe3d5fbf45f9d0cc4ff0f055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187856263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f8692338efe9c020233679268173bc6900d291064772aee0d9df63887fcdf3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2efa8ce97d282fc76ea2985fc31102becef655447ddbf9bdd3209771347a0182`  
		Last Modified: Mon, 28 Apr 2025 21:11:27 GMT  
		Size: 29.8 MB (29825462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc02d008cc6afed9b7c3969b1acfadb19a81f979629ad24260fc17bbe6e1ab8`  
		Last Modified: Tue, 13 May 2025 18:39:49 GMT  
		Size: 85.2 MB (85216749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f349aad2f69fe19dbd9385742a456010d08ceabf2aca5e61f751bb06c159a376`  
		Last Modified: Tue, 13 May 2025 18:45:35 GMT  
		Size: 72.8 MB (72813009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fae67b7314cd6e4cd4c3244f8dd14fdbd7218dc5bcc1652440ac03bf3b98843`  
		Last Modified: Tue, 13 May 2025 18:45:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407cf07e88b430835671fdc438f5fccf5e350c9f346f9a2824d722a18fb5527f`  
		Last Modified: Tue, 13 May 2025 18:45:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:82985fab739c781ae2fb4bc94ecd3ec4d10d5570316fd1098283c0a018f344bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5031653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdf99361dcb7d45b003d6f89be7b0ee09748f7143b2d8ccb1fe6275c9d992f3`

```dockerfile
```

-	Layers:
	-	`sha256:af824ad97fa73a41ddbfce8b2443884f2db9c2b650464e5e9fd20958a94cf7af`  
		Last Modified: Tue, 13 May 2025 18:45:33 GMT  
		Size: 5.0 MB (5015805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d045d367dc4f17f22449317bb9504d3592a2cdf9fd638857724182f7dbaf0895`  
		Last Modified: Tue, 13 May 2025 18:45:33 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json
