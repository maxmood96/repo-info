## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:f9a5ae37c2d9b7f8fc8e29742c6c8b5ba848d1b052f4ffd24c5e172ed9b0fd58
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7ba0f25e65fb5751d40e2983821d7589166b14eea4ca8eaac75b3815777d8d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274476813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584b79b1fc6469460088f2fb6e56875ecf4aa4b42d2e1ab5cb3e775c6e818f89`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:43:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:00 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:43:00 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:43:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:43:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:14 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c18ce2d1767bde40703df04a553c0bedc6e423feeb29d9c1743e9a1b1263d83`  
		Last Modified: Sat, 08 Nov 2025 18:43:37 GMT  
		Size: 144.8 MB (144848032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d586ebc115fefc8de6a7c799c09827aa73b0839b4d94b40b2bc265d8143f570e`  
		Last Modified: Sat, 08 Nov 2025 18:43:57 GMT  
		Size: 81.1 MB (81146683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536eac243a5e1dfc865bfaf75b2eebd8aa09248eb203e58d779249ac4bdba871`  
		Last Modified: Sat, 08 Nov 2025 18:43:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b1d8cfdc2504cce39d0f85d03753e1ce05c82e925dae3777a9987399e03f48`  
		Last Modified: Sat, 08 Nov 2025 18:43:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0762220b855d95f2c8e3521787de77f3e5e269134513b9b776a604fcb53fa194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794a5b5620a12b19e99d501a594a95ff23268926102a9b27f630773aebcff38f`

```dockerfile
```

-	Layers:
	-	`sha256:4d5cd05cc0f8e4ab4302f939ae19b0cba28d6508f22cdae3b391b410e518150d`  
		Last Modified: Sat, 08 Nov 2025 22:40:59 GMT  
		Size: 7.4 MB (7374892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86caa41a5915dedd28ed62bf8897c2e759e50b6c201117249049a041b3bdf32e`  
		Last Modified: Sat, 08 Nov 2025 22:41:00 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78a967c1bd6ebb76a968fbd70a428d0634feba8f0f4115f72b969184fdd40442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273071610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc28f23c2dae3a763bbc5c80e419fe5e25d3566f5dc920f07eaf9464a68eb396`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:42:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:26 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:42:26 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02779de92cbe40f2440c934503688b46946311c4ce317a946f5c5d4caa912112`  
		Last Modified: Sat, 08 Nov 2025 18:43:07 GMT  
		Size: 143.7 MB (143680053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807c5c469af39c2ee9f4d6e172ad346430e29b8199ef5fb5a14108577bac164`  
		Last Modified: Sat, 08 Nov 2025 18:43:46 GMT  
		Size: 81.0 MB (81031036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85585b35d915eefe49f0947ce9d9cce13ed4fe305de08cdb0e816f63b6125bf`  
		Last Modified: Sat, 08 Nov 2025 18:43:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b2efdf678cd7734f43f15c7556ad0fc554964f5b626ac75c30c78f0efdb6b8`  
		Last Modified: Sat, 08 Nov 2025 18:43:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b095ac87804fc043d76dde5dfb4ee9cfe31ddd04a1bfa6fd692cfe988087ba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16905c494c92dd02ad1559e611bb6642ba7f4d13226dc0d5f671e9af2862443c`

```dockerfile
```

-	Layers:
	-	`sha256:5b946ec71a99474c84fd33bef0f4e53173833a5c0dacedce8a724d9df2501a84`  
		Last Modified: Sat, 08 Nov 2025 22:41:06 GMT  
		Size: 7.4 MB (7380655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf294dd512766e3a8bad2e88c77496cd214b08bb3a3f191a9789bf742247b67`  
		Last Modified: Sat, 08 Nov 2025 22:41:06 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:964f6887d642cf3aa390292de0e39b47a5a5616cbd5998049d8404851121c8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283839481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f88884e39a16eea0bb0d17510de6adc831deb86cbc50e822551f5493643bf1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:13:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:13:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:13:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:13:32 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:22:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:22:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:22:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:22:02 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:22:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b991744392cdb392b2eb2934ca9a948480035c261ce99f62fad6bd622bfcaaf0`  
		Last Modified: Sat, 08 Nov 2025 21:14:39 GMT  
		Size: 144.5 MB (144525137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d38c6f617e0c6c8d09cdde56fce237a7770d47e8c84745692bdcaaa3ca7fb38`  
		Last Modified: Sat, 08 Nov 2025 21:22:55 GMT  
		Size: 87.0 MB (86986024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11b7fde61805b5a0f91d90569c4ff1d2941fb9a48e95c756e5795d7857a6e36`  
		Last Modified: Sat, 08 Nov 2025 21:22:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a0bf506f738194304e84a4124d9e125f1f7ee59f251e94193f46511112764f`  
		Last Modified: Sat, 08 Nov 2025 21:22:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:769b5ed7bd4d11b143fc7854b5405ba98ffcdfed3a377c3fab63e6eaf04a234b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee6d44425207466815a8ae7a7e63e6ffeb93b7b8ba025d8814837f4c6017110`

```dockerfile
```

-	Layers:
	-	`sha256:f6a67c71ef950509a41a1ec29761162ff442cf32b5d0a0d2b39c1d2ad1818505`  
		Last Modified: Sat, 08 Nov 2025 22:41:12 GMT  
		Size: 7.4 MB (7380106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:795b2011fcf39d6268643521d6721af27beb0d57ded8bbbf4ba0a78191849d36`  
		Last Modified: Sat, 08 Nov 2025 22:41:13 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:b7e87356a01f18f8f697dc02383d7e7d4d9a282c24e0f1dc275186366d5625e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261954759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f692abe793b0f44642dce708af6f46652aff860e0e1ee393f6686359ffdc995`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:35:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:35:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:35:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:35:45 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:35:46 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:41:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:41:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:41:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 19:41:45 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 19:41:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c081acbe0e53579c655776769c55de0a79d0fdf1ffd7568881985607f4314`  
		Last Modified: Sat, 08 Nov 2025 19:36:30 GMT  
		Size: 134.9 MB (134858996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733201497b76d5d073bf92d7e5672cdb739f85d401fc64b7314fd03a4a0cc213`  
		Last Modified: Sat, 08 Nov 2025 19:42:24 GMT  
		Size: 80.0 MB (79956632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a1b9756424e7e409751d1d591ee937275dd810cbe9fa442ec784a2431c951b`  
		Last Modified: Sat, 08 Nov 2025 19:42:18 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f85471d85e62167b54fe12aa2986ab03632be555145e21c3b6fbbec4f78c1cc`  
		Last Modified: Sat, 08 Nov 2025 19:42:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a255283cbc8c7577fda72ad7273e50a9602d9b5d5600013575c1d6b090e81411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb1d0f3b5afcca99124780a2ba822cd39064b4f081a90aa3a80e3a2e8cee0b5`

```dockerfile
```

-	Layers:
	-	`sha256:bd4140698212c6c456975d21bf02a40f135dfa261c5a00dedeae79464ecb9d75`  
		Last Modified: Sat, 08 Nov 2025 22:41:19 GMT  
		Size: 7.4 MB (7366211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6b4c193abde35e99317f70d4921f740a4fe2bd97daa64254c2f154810a5286`  
		Last Modified: Sat, 08 Nov 2025 22:41:20 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
