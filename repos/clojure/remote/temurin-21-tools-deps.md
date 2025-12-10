## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:668c2b9c4d381d3966428765fe2dd696bbc2b7d5635becf540cc0359b011ce68
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

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:a9f22942f79497ce3d3701b01241de652513d5c09967175d1097f97180f4fe31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287453708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38e3a9a360ebc94b56808f8669780f2927399de0413413d03de504e0685fa55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:54:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:54:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:54:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:54:53 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:54:53 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:55:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:55:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:55:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:55:09 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:55:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d974c063f21030a11891ea31c9c7f21e6c4c68e43c850c0fabd168133b06`  
		Last Modified: Mon, 08 Dec 2025 23:57:43 GMT  
		Size: 157.8 MB (157825976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c177519310618649ebd57b758125816a30f0ae5b5170828be18c24ed1cc264b4`  
		Last Modified: Mon, 08 Dec 2025 23:55:48 GMT  
		Size: 81.1 MB (81145957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d061b9fd752ab5e35cb3f0a696b97b6dfff086999bcec6e61f838caa36dbfad2`  
		Last Modified: Mon, 08 Dec 2025 23:55:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8eb3c4d0e33ab34b2293038e49062e02feb559be7a352706a7283c2d6cad55`  
		Last Modified: Mon, 08 Dec 2025 23:55:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:da56208c262a32dcb85f03d6ce34e7e6f8731f73b3c6b1eaf6033fab34c315e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ebda3042adf889e9554187987fe5e16fb5c5528e9a26b6c6d073be4150a1b8`

```dockerfile
```

-	Layers:
	-	`sha256:54529de296c3072cd4b5684ec7ef9101375f27228066013fb5010d6772b8e5b4`  
		Last Modified: Tue, 09 Dec 2025 04:42:14 GMT  
		Size: 7.4 MB (7378678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47408799eb23248360850fb32aa8b5cb0fe4fb69eb4029f386eebfb4a350ada3`  
		Last Modified: Tue, 09 Dec 2025 04:42:15 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aee720b59ba09ca6e9f2ed4fad73a1b76a9f13050ccfba0db585912171efb756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285498694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f57473942d621bea98ac5fe73ddd9e69768b354803a444a961d326746798f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:02:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:02:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:02:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:02:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:02:20 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:02:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:02:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:02:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:02:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:02:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d612743c2d42369d3128f5d2f36f8a5e4ed051e65c6ed758a705187672bb80`  
		Last Modified: Tue, 09 Dec 2025 00:03:29 GMT  
		Size: 156.1 MB (156107673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcca37306ff16fb10dfabfc32105f5459fe302eea4b1066df8d4213ee74ee53`  
		Last Modified: Tue, 09 Dec 2025 00:03:14 GMT  
		Size: 81.0 MB (81030909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4295b101a5c87697b6794ccb530fc2d6804ccae9cf8bfa1a3ec96ba02d09b8fc`  
		Last Modified: Tue, 09 Dec 2025 00:03:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9eec46754b76f76b9619c19f0e5b1906b77d1e1c05b8dcec886c10f57ad690`  
		Last Modified: Tue, 09 Dec 2025 00:03:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:5848436e1f8878bbdb0aa9bbd31f5b75ed98e9f535cae07a33478229a3faa774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0d0627277bf9db52a105ed82be5a52ec13771118f2dd17d71a4ad80b3f04c2`

```dockerfile
```

-	Layers:
	-	`sha256:9cc2bbe241598b3a99d72b07b021a7bb982bafdd538340edc5ff254382a7ba45`  
		Last Modified: Tue, 09 Dec 2025 04:42:22 GMT  
		Size: 7.4 MB (7384465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9f6a99b9c9d5442856a80d2feb20f6f3914aec5f54dacdc7ea89cb34667c875`  
		Last Modified: Tue, 09 Dec 2025 04:42:23 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:7fbed5844ba5f0d92e16508736f1e95236dff4e701d5bfc84a50fad547959b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297257026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ab04be2af6916ef281a6948c2aaed22c6ad5253f7e9fbf9506e3218c2e82ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:44:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:44:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 22:44:05 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:46:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 22:46:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 22:46:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 22:46:39 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 22:46:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84193563598712b437e18d1f55a29d0760b80aa62c9cc1125eb6b86822607f7b`  
		Last Modified: Mon, 08 Dec 2025 22:49:33 GMT  
		Size: 157.9 MB (157942939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bcfd0969310acb7645731a9925226b7a2b9cfe8836dac58830fd18fdc8f455`  
		Last Modified: Mon, 08 Dec 2025 22:47:40 GMT  
		Size: 87.0 MB (86986069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e381794b01c7a240ba322101311493e2263d48532004b9020d815c407f5add`  
		Last Modified: Mon, 08 Dec 2025 22:47:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c72b91bf46d3e638e266d83880ff23cc9eb808669ce56276d72dad6c6ef304`  
		Last Modified: Mon, 08 Dec 2025 22:47:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:cbd515b544b930dc97f4fd9fb269c75a195da396a2db7ef8d34e8e156efba463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b627e11258b5d870a9fc16095e413263dab58d323ffc44e6beb66dc552ecf6a3`

```dockerfile
```

-	Layers:
	-	`sha256:c97f79ec76fd9fa0e67bdc50c6e4d6271f9728ad813a74b0f36ba87c08812995`  
		Last Modified: Tue, 09 Dec 2025 01:37:32 GMT  
		Size: 7.4 MB (7383904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:177bfafb4b7741e6ee04a25fdea36b3fecb92066ee841b159cdfb17cb27efc12`  
		Last Modified: Tue, 09 Dec 2025 01:37:33 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:5cc3f7f99384a7cdc13fbd3081fd9639042eb2deac8974a2bee73d6fa798be9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274165066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad8d853d95d515f3a43cfe237bc33b1b9e40cef9c40459ded2dfc0ee1af42b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:30:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:30:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:30:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:30:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:30:38 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:32:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:32:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:32:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:32:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:32:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0989d7c9aea3b9e5f8aa3bfd4c0ad22e264c7b070ed172dfa35b1bac1415808`  
		Last Modified: Tue, 09 Dec 2025 01:31:52 GMT  
		Size: 147.1 MB (147069832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75eecf137c51ea353a85534daa3b470ddae91693d6a11a03868642960a112f14`  
		Last Modified: Tue, 09 Dec 2025 01:32:51 GMT  
		Size: 80.0 MB (79956531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5cc533af05e7369eaf1532fb086233d089a0186471128ad74b0c2b9a8d7831`  
		Last Modified: Tue, 09 Dec 2025 01:32:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0240a1083a9c50bad83e8427187014e87aac09b7fb2fe31ec26e87468e832ecd`  
		Last Modified: Tue, 09 Dec 2025 01:32:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:1aa829df50ec0397367bb983021c0608af070649ea25ab5d8c0d95baf466b243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a933a16c2d8c2f61b084e82ee9a390db477c825bb1d78ec4ca78c4915d09d678`

```dockerfile
```

-	Layers:
	-	`sha256:1e72a51131a7132c46e8ad4500b4de8f851be2ad9022e2342a7870957be1c124`  
		Last Modified: Tue, 09 Dec 2025 04:42:33 GMT  
		Size: 7.4 MB (7369997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2e857c7c9932b06300d2bb687dfb1565f5b1af50b629e6d89a8d9be41bd90c9`  
		Last Modified: Tue, 09 Dec 2025 04:42:34 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
