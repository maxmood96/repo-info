## `clojure:temurin-11-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:eb77a93ba1d19e384b966d4a0068282b2d557df4d152b1049e5fe8435ba6efe9
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

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:a807c05e4314bcfdcc7bbb4ff318de66c5711431b8b1a508c58208e2dcfbae8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280672490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130fc217826ca940635f266b53852dea6dcdc3ee2aad80fefa03e30fce278740`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:57:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:57:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:57:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:57:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:57:38 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:57:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:57:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:57:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb54510be5dd529a45491b2d45781a2ef8293dab138c2df896c29119a09feaf`  
		Last Modified: Tue, 17 Mar 2026 02:58:18 GMT  
		Size: 145.8 MB (145806906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def60eff5b4e136daa2c237e54a688b0b099d296227bd0bf8d0aeb2ff78e11ce`  
		Last Modified: Tue, 17 Mar 2026 02:58:17 GMT  
		Size: 85.6 MB (85567412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d0821a984e6e30b82fe2d197396cf9daef7e4846410906c64b7aaa8848d7a2`  
		Last Modified: Tue, 17 Mar 2026 02:58:14 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c91a0d60ede5d35449932a1865236db59f8a40d0d0d1a3519f570337fb719ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059d43cfa6dcc90c9b80cec31f4e45bcb01fd3788ad2a9653c65856987cebf1e`

```dockerfile
```

-	Layers:
	-	`sha256:9c533de71aa37cb372ed78c4c7e51746e60b6854a849005b094feedcd4b33422`  
		Last Modified: Tue, 17 Mar 2026 02:58:15 GMT  
		Size: 7.5 MB (7490808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cd670e70a10a510a5c6fde30347103fa0e7967fdac48b866b70db31f90203a5`  
		Last Modified: Tue, 17 Mar 2026 02:58:14 GMT  
		Size: 14.2 KB (14183 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e9f38e197e70b18d56cb4adc0dd4bebdf3fe612266fdb15582c50a8e01fa2efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277548524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bd399c61805fc3b3f56d1eb9d7810d774dd4b9dafcd20df78751002f320b90`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:02:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:02:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:02:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:02:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:02:20 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:02:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:02:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:02:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa6288784eb74a6ba57e6286058357a72d683a99bd88e42cf421917c580a781`  
		Last Modified: Tue, 17 Mar 2026 03:03:04 GMT  
		Size: 142.5 MB (142500013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a566956f595719f86efcccdffacf6d43e8ec3b5be5a0cf1eb2e0461501f41fa`  
		Last Modified: Tue, 17 Mar 2026 03:03:03 GMT  
		Size: 85.4 MB (85382913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab6773f4acd7f1863aba6afd3fed952ca1372b9aa8c51ca87b2ca7bc0923381`  
		Last Modified: Tue, 17 Mar 2026 03:03:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5246691694ada2b3898ba1c94ea8d56917833f29be7ad8d6afe5182519214690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46727210d50808588e5a0fbb22a3209ffa94666bd7097152d9f099b618ba557`

```dockerfile
```

-	Layers:
	-	`sha256:ff4f81c8f63daf85aaa178efff734cbb2a4cbef0d718f2d49a13c40741f4a129`  
		Last Modified: Tue, 17 Mar 2026 03:03:00 GMT  
		Size: 7.5 MB (7498456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708417619e1bab09ecbe9a605739f6ee7673720015f96119ea90170224d27222`  
		Last Modified: Tue, 17 Mar 2026 03:03:00 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d4b68eb3c372e5590d89a4122f1d24ce7e12894f6de00a45b3cf0b4df4839071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277087554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16320fd254b41173dc3cef15fb1d206fcba7728a8555009cfadb7dc9ef6390c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:48:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:48:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:48:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:48:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:48:56 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:49:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:49:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:49:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d9812c3c8a7294cb0d2f7e16091ac0a9f181006c6d424360a6b8af498eb9d3`  
		Last Modified: Mon, 09 Mar 2026 20:50:38 GMT  
		Size: 133.0 MB (132997823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d343ec85f214f649c22e83cd7553169f67b505368dfdfde4ad5637064bdccd3`  
		Last Modified: Mon, 09 Mar 2026 20:50:37 GMT  
		Size: 91.0 MB (90976825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3a7cda731543b5896ba90787685df40f8226ba9ecd3cb56b6858b67c7e5079`  
		Last Modified: Mon, 09 Mar 2026 20:50:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b906ffa3ef032eee2e06cdd366c25ccaca4ada95881b0d929188673e38da9d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7759b22811fb0cd6b150186a5e5f404c0d0fad76d76334d1432fcd4360250005`

```dockerfile
```

-	Layers:
	-	`sha256:95e28823dcfbfacee08eb43ed22f40d79a342034bf16755e66353e42aa473761`  
		Last Modified: Mon, 09 Mar 2026 20:50:33 GMT  
		Size: 7.5 MB (7494540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3bba833f64e369bddf4cb5d6705af1b3da9700c4421cd8a8649e5e9fb81f69`  
		Last Modified: Mon, 09 Mar 2026 20:50:32 GMT  
		Size: 14.2 KB (14232 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:628bdb638232a82426b4218d884623f7910f83c97ac00f15c3bad029e57e9f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262447214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfa3bf3c3416533c62f91644912c927e749f9ec2832912f405448da451d8257`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:33:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:24 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:33:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:33:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:33:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9426dc6572863c0a325dcbdc9d248dece97f4bd9dcfaf1a9a35a0a618fb8da40`  
		Last Modified: Mon, 09 Mar 2026 20:34:16 GMT  
		Size: 126.6 MB (126562061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad22ab1d74b002d476b1f1bde295e04aa249198ce5849cf19b8a42733e43250`  
		Last Modified: Mon, 09 Mar 2026 20:34:15 GMT  
		Size: 86.5 MB (86529974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202fbd2ab3d5be54905ffb183920b0b2026f1a86a55f412792f72ea01a56fe0e`  
		Last Modified: Mon, 09 Mar 2026 20:34:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1ae4a60ede9fef6439d1cf8df1700f25898f1643d4aaf5591827a7d7dbd60cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79550fd77aa25940ac085f3ca06e4de82237e5ab943f33f9e5ab6e83552fdaf`

```dockerfile
```

-	Layers:
	-	`sha256:e2de221383aaec961857c03c9bb7f7f9eae9366d6722c63af304425d7c9e0f10`  
		Last Modified: Mon, 09 Mar 2026 20:34:13 GMT  
		Size: 7.5 MB (7486660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4cbd0cd611d67468062ee19be0f47be34a79c59bfb9812041412be13b23ec85`  
		Last Modified: Mon, 09 Mar 2026 20:34:12 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json
