## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:288cbe004f4e6807c1a595cb086af575135d8f5957c700b11ab8b1d574fd0bb0
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3722cfc6f3e70c7bf9284975e6c0207ea436f31776294a868e1acb49477c2e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275473676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb282a788ab2921a59778773b11686079daab1444dd03baef1cefcad9d952e8a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:13:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:13:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:13:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:13:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:13:49 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:14:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:14:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:14:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5175e430b4963729228568a2df05e2a48e80867ff42eba0097fcd44a35113117`  
		Last Modified: Tue, 07 Apr 2026 03:14:28 GMT  
		Size: 145.8 MB (145806914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548783dac94a7ccce28621cd868293d7ccc695f313d45a3c5ab8c422f179d5f3`  
		Last Modified: Tue, 07 Apr 2026 03:14:27 GMT  
		Size: 81.2 MB (81177293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5276eb8c7ebb04289a571d02fe2d35efcdc54d37a52a750c4e94770680160`  
		Last Modified: Tue, 07 Apr 2026 03:14:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4ebe8e33205049b070a06241b3729cba7fa83fc0cda0a4e115b5d0212e214b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf8872ac81bed7d27ab53d32c2a33bbe059d170cb22cc5d8f2cef6089fa7bc2`

```dockerfile
```

-	Layers:
	-	`sha256:3be65f4226c94c8acbb393e7a629f4f2eba788f6e70083cbc6a795bc5dfe7218`  
		Last Modified: Tue, 07 Apr 2026 03:14:24 GMT  
		Size: 7.4 MB (7398443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0404fd1e1e59251afd6a915a2358194e9dd62aeccb6ebf3eefd7a65df9fd8c6`  
		Last Modified: Tue, 07 Apr 2026 03:14:23 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a3f8878b84c6569673473c53e1a7716aa402b9331cf9d3280780d362aa52777b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272032485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922c70d0ef29e70606b3872ab8e789ec196b45ff74800d11cbd60b3442704402`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:24:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:24:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:24:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:24:34 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:24:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:24:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:24:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b303ff6508db6b1bcd5cc0250e99937c8968bbfe4390ab1868b687a1e6190f`  
		Last Modified: Tue, 07 Apr 2026 03:25:24 GMT  
		Size: 142.5 MB (142500056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4883d604493eb9a58899b1756595364edc9e7d3eb511b5558c7c1b52baf2fc`  
		Last Modified: Tue, 07 Apr 2026 03:25:14 GMT  
		Size: 81.2 MB (81158520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcc7ceea6bd85bcd52cb7277839cda1fdd4bfa8760505cbec173fd546bee877`  
		Last Modified: Tue, 07 Apr 2026 03:25:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:608b2405c2f4fcb59c9bf7e1de2104697f41935af877bd7da16319c1623694f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09bad6d499d6210264a106282d1c62bfacb914e3fa46d9b15df6b5d90222b69`

```dockerfile
```

-	Layers:
	-	`sha256:ed7ed19534817c6500e9d8a416cdf8f6a2ec4a07db649f3e419489e5672eac01`  
		Last Modified: Tue, 07 Apr 2026 03:25:10 GMT  
		Size: 7.4 MB (7404824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82915aba743c7895d0153f61e465e8044b1261d6ca7043849dc74e5715cdb424`  
		Last Modified: Tue, 07 Apr 2026 03:25:09 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:6fe193a0f68ae9e6bb9afd10521f8e14953f489edebda52f8d2ca3d88f3aab92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272334171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711e0d6349cd22833e654d9d4016e604ce375c79f5a1abff11dd09d4bcc7e09`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:15:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:15:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:15:42 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:20:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:20:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:20:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbecbf7ecf5689b9ec9a2fb7833196c9e479474539bbea61e477b10fa3c1a715`  
		Last Modified: Tue, 17 Mar 2026 18:17:05 GMT  
		Size: 133.0 MB (132996700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be671bba964e222550568c709017ea34bf00ad187b011426ef729f2058c5d8f`  
		Last Modified: Tue, 17 Mar 2026 18:21:29 GMT  
		Size: 87.0 MB (87000129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195551047080f5e747289317b95caac03f79ab8c8ff94f15d57a3e5f8a6bef5f`  
		Last Modified: Tue, 17 Mar 2026 18:21:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:abb4668bc0dababe5131336afbe221966abbbd96de112ff798fc858641d581f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58e10dffcf6683f7a31369d1f3e1b96fc5f5f17da7566799d6e6753641e39a7`

```dockerfile
```

-	Layers:
	-	`sha256:69e2984996075424fea7a6b33e8eaad5b650a7823143e43f8a915c61593494e5`  
		Last Modified: Tue, 17 Mar 2026 18:21:27 GMT  
		Size: 7.4 MB (7403044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4633d921cdad0f6d3e596f76035fbd08f71f5c8435af9df311d211cf0280ceee`  
		Last Modified: Tue, 17 Mar 2026 18:21:26 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:885addda74201b1f06c262da677d9300b23004e93a14048f697782c670bddaed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253698678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178fa9095d9a446892a4dcbceacd88d56a9859ef3d0849e11731290731cc8e1a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:40:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:40:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:40:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:40:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:40:08 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:40:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:40:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:40:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cbf6ffc38d826dee06273c7ef7b49d6253b226b4fd09999f110e03545066ff`  
		Last Modified: Tue, 07 Apr 2026 05:40:51 GMT  
		Size: 126.6 MB (126562219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcf6b342e10a8b2e1fce7bb6bfeadd0e0e9370158e708eb04906b5b344c1cff`  
		Last Modified: Tue, 07 Apr 2026 05:40:51 GMT  
		Size: 80.0 MB (79987728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2a01aa53cd7980f006f601ad8d3ee9a4192900b64c7f58d39ae362b5feaf07`  
		Last Modified: Tue, 07 Apr 2026 05:40:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:46401c905fbe8eae63ca0cc0adb6e3528583d95774b81198fba3490ae25cfbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3eadfa87710b435bb220c1ed68b5dfbab15e90fe38690cc72a62dc62c68e53`

```dockerfile
```

-	Layers:
	-	`sha256:e9b9d43002641857b5012bf77823c46911a08ec84948c9dd84abce916d2d0b2c`  
		Last Modified: Tue, 07 Apr 2026 05:40:49 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ef1e06e39e152805c6c31d5f2684798cd0c0347f5b200a98732cf9a5dc02c4`  
		Last Modified: Tue, 07 Apr 2026 05:40:48 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
