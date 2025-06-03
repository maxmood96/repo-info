## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:fc1732c50ba5dca59691a7815b5bdb85ce0b462fb2085ffed16767efca608fbb
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:8752f0047d74bb72bf3888ca3875a3ed202ff347e7df1a75844ba9ccd7a050e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283105536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3846f2cb12e6ddd7e183c9927fa8db0357d7c3d8f134096490373405218f4600`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435adb4c054b5edf3d6776553a009a610f56ed44dc0a40c3262662c9eee967c`  
		Last Modified: Tue, 03 Jun 2025 05:16:05 GMT  
		Size: 145.6 MB (145635638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317448e024012e5bb817e000096b90a3f75492e581c25ffe6950698fb859e41a`  
		Last Modified: Tue, 03 Jun 2025 05:16:06 GMT  
		Size: 88.2 MB (88222348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9efc8e2d6b25df02dac3913e3b1817ab650024ac0fa6bb949abc455fffaa2c`  
		Last Modified: Tue, 03 Jun 2025 05:16:04 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:98066504ab18c761a1509f0457bf9589810914158777190c4ef252b267e43d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5b0cfcba7d17cb2e6408149a3fe02c1c7e96c938545ee599ad674f425202d1`

```dockerfile
```

-	Layers:
	-	`sha256:31da7ee00e4e3e76fdc06c78c567bf8798ea7f21be741199ff26f53176bc46dd`  
		Last Modified: Tue, 03 Jun 2025 05:16:04 GMT  
		Size: 7.3 MB (7338557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43f5f6f1c60ff83e2584aa0427b1125a5e60b92875acbd2c3a8f9fe0cf599ef`  
		Last Modified: Tue, 03 Jun 2025 05:16:04 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8063b461d0c82e859eee6e8aa32e9e816747bac83e8fcbfda8bdfd1e50a2f812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277214897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab516b07f20ac5f880a3e584de5d419778eabd1d01d257342603648ed4a5af04`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Wed, 21 May 2025 22:31:07 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fb27b90b3828e5b95e6f507607ede8d9b516d361aa57b7d7bd47780cf9df52`  
		Last Modified: Thu, 22 May 2025 08:12:56 GMT  
		Size: 142.4 MB (142420737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b4c740d481bc7cf1d2cb962ab1228a851ed52db212c6b162a8fc0bcfcc0f0f`  
		Last Modified: Thu, 22 May 2025 08:17:22 GMT  
		Size: 85.2 MB (85175221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae5bf51efa6465c109a8e640cd5b844c50c521b6cabeefa4fb68eb4ee32d1c1`  
		Last Modified: Thu, 22 May 2025 08:17:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4521315609bf18b024f34d086171b3646c4ab03318d73b9a81a110989dde4251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fb8b5536537dfae29558ae169d24a01308968d61774191a9c03bdd669e067`

```dockerfile
```

-	Layers:
	-	`sha256:f60439b48bfe0d296ee6f517c2940d9d6138f434533bc312b3ad8a8927172737`  
		Last Modified: Thu, 22 May 2025 08:17:20 GMT  
		Size: 7.3 MB (7346205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f1128932af124ca833671175b8c6f9d6d09def700e5b45930e591149c26415`  
		Last Modified: Thu, 22 May 2025 08:17:19 GMT  
		Size: 14.3 KB (14345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b98803cb80976b0a8bbefc7e871cdfd4891ece0f2ff43df20c3d01b35351af05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279848653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138a46605148488bc6d3c904746a2faf85f89887c9e5298226fe9fce784eac48`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Wed, 21 May 2025 22:32:01 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39291d7ae4a9e82fc2c95d75539cc21cd0bc9715c3ac4d5b032793f128324bb4`  
		Last Modified: Tue, 03 Jun 2025 08:31:55 GMT  
		Size: 132.8 MB (132810533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58aad42ef21992f662582a9ac2f7e2977cadc5a0420488acdaa013fe17d1150`  
		Last Modified: Tue, 03 Jun 2025 08:41:08 GMT  
		Size: 94.0 MB (93956933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3afa180df902b1950504b9800c3144272d1b37c9e82b9b4abc12685e979c8`  
		Last Modified: Tue, 03 Jun 2025 08:41:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8df447e792fe80a8011e07c5817e13fec2af12cd67298a4a39a027bc8d71d7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7356635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cf8ed4000888f8a927bfcf8f826834c7234130f9c0c82578d8ccab3041d208`

```dockerfile
```

-	Layers:
	-	`sha256:e1d3071903ab09753a842fb9c1a4bcd01bdd6a1ca33011e2570f0e1131c1185a`  
		Last Modified: Tue, 03 Jun 2025 08:41:05 GMT  
		Size: 7.3 MB (7342359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd4cd35f363771ac403bf6bf38a96c7631ac7c30f876ffe047e899ce646dead`  
		Last Modified: Tue, 03 Jun 2025 08:41:05 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:9a9ab9cd97a266ca86be76cd20947cf5fbf3df8c05eabd57485c62893b119c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263859409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a74587c1efa1d1b4b26afb03d7f15fdcfa2068771b5a751448b4b1b97825c2f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Wed, 21 May 2025 22:31:46 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3809b7d5c48c969004e20fea95a6f198fb053f68fc077ceacfe71f6d2bf50ddd`  
		Last Modified: Tue, 03 Jun 2025 06:04:23 GMT  
		Size: 125.6 MB (125585319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f572c854d4e11a0d7c2ade3578d22b5e20ef7118cd0f7fb2f7a130d1be660fcc`  
		Last Modified: Tue, 03 Jun 2025 06:10:14 GMT  
		Size: 89.0 MB (88951218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92922a2cfcfa93357e350fefa86bca763124804d796e0030e9d027b42992d7c0`  
		Last Modified: Tue, 03 Jun 2025 06:10:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4cbc8c5c5ad0cab1718afe784bcd8aed8a33043e4901d17c42b0ac6a2e870d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b168997de513aaf85860b808d084450bdd16d727efd2e13749785708564161e`

```dockerfile
```

-	Layers:
	-	`sha256:c789648c7873e36d7db61ceb955cf42e36c01ccaa193753576e8ae20017f7954`  
		Last Modified: Tue, 03 Jun 2025 06:10:13 GMT  
		Size: 7.3 MB (7334483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2ee176893bc743730c82555e6a3bcdaa685cee5c4fc8def5ef03981a5411ea`  
		Last Modified: Tue, 03 Jun 2025 06:10:12 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json
