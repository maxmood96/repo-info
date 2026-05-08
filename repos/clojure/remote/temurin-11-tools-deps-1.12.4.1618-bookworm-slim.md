## `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:da22d5eab34dc42430a7a8cc1212bd7d6e418e3e16fc131c1c90bb56e41cf604
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

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:480c0587ccae65462a6a6a1a280ddcc3c2c9ef9ed9027b03ef75018ee6d6d9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243822298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fae29f1271682c713d85d2ef6f4c64a77ef614e3bffc2ed7e1f8f331877a3c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:06:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:06:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:06:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:06:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:06:20 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:06:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:06:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:06:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bb88c05aa206efeced6d10e14359931afa5610b84df105a7c8a364f517e24f`  
		Last Modified: Fri, 08 May 2026 00:06:55 GMT  
		Size: 145.9 MB (145886199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c968ac6de23304d7f9b422dd29a85d06f42cf0e35867a03c332a613969fe33`  
		Last Modified: Fri, 08 May 2026 00:06:53 GMT  
		Size: 69.7 MB (69699202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88808ba2a1a95ab1eef5f74455d957182bf6365174e34055970d795b7d0ad6e4`  
		Last Modified: Fri, 08 May 2026 00:06:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:931d9b03fac5050030b6c48a08c2b899a1d8f5f95bfc09c8e75de0ae2c2125f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71526f16155aecbf92dff35d4aa262d4f9eb4506a8de2b976a1bc7e6e31c050f`

```dockerfile
```

-	Layers:
	-	`sha256:30fe6bb83dba1b80d01fd7d1f48a21e0adcb61974f8673350ae784cab7ffc31b`  
		Last Modified: Fri, 08 May 2026 00:06:51 GMT  
		Size: 5.1 MB (5136310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b042936926d795265f41edf4cbbf293de41cd8d03f2524abda43531a97556c`  
		Last Modified: Fri, 08 May 2026 00:06:50 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:439914fc531edc4ba936aeb073f5d756159eac3462c5a7ff392ee96c2a79fc07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240391611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003c1a3e1bbab6432069c9315d14ca7fb0c05f5dcdb1ba9cb3320104b7eb358c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:08:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:08:32 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:08:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:08:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3b940a2dea035839235250ff0729470741a3a5d1f593458a8ffcb8a3df9a07`  
		Last Modified: Fri, 08 May 2026 00:09:08 GMT  
		Size: 142.6 MB (142582244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c44728bbbe3844a97b5a4b648870f257ae597dcea4fd5b064ec6e1276f4ea8`  
		Last Modified: Fri, 08 May 2026 00:09:08 GMT  
		Size: 69.7 MB (69692608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdb198ef95c7e75885f278911bb0abc21e529c4798f706f3f0aac323b73d267`  
		Last Modified: Fri, 08 May 2026 00:09:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:04cccc1dfaf028f8b7d42e8a28b9d04e494de35e30b3bf6f846758d71b139a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129d5950ebefe5e39398fdaa9e22cebd33c20a6ff9e6df33e6a1114d53bd2035`

```dockerfile
```

-	Layers:
	-	`sha256:1f196206b4a8cfea8cc9cc320f04aa77bd3d0c196f2c969ba7973e296d5c7de4`  
		Last Modified: Fri, 08 May 2026 00:09:04 GMT  
		Size: 5.1 MB (5142689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee244c859add51987c49b07a763ee7e14eaddedf6308ec27964006cadc272802`  
		Last Modified: Fri, 08 May 2026 00:09:03 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ba24923b95a855b00b82a4ce2c2060a3ab8b065a589ef2662e6b807447190043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.7 MB (240719028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e58efdfdcfb529a70201a2c941f34d93c59a69e9e0726a151fc76e8fa17daf`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:32:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:32:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:32:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:32:03 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:40:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:40:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:40:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76ccb486cd38d4bc6e81d6a758dc0756e8388df36970ae898570b04b2565a95`  
		Last Modified: Fri, 08 May 2026 00:38:30 GMT  
		Size: 133.1 MB (133110145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adffce10ce7f47262ccd902072eb5c37ecb1f357ea732e36b40cd7d3ef58b14`  
		Last Modified: Fri, 08 May 2026 00:41:37 GMT  
		Size: 75.5 MB (75529836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26258ca5b18a373e77774f7a4c735d81a332d6a071fd7342ab6e8cbd7892b77`  
		Last Modified: Fri, 08 May 2026 00:41:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dafc7b16f2c8534a755bfb04f60c0d3e49f6bb055b4896b00f11115968c86f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8650cd1ab9e4ca3f5b440f6e2940e02475e616307f7150e8436b23c18e3d55`

```dockerfile
```

-	Layers:
	-	`sha256:b2ba33bea4ff533a3255fc53d187aec7f40ebe56ab29788f3c5d1d745d28c2bd`  
		Last Modified: Fri, 08 May 2026 00:41:31 GMT  
		Size: 5.1 MB (5140853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d98e25fd155844e96c7fefec0337d88af0b0a71e30183558d327e3fc5adf7d`  
		Last Modified: Fri, 08 May 2026 00:41:31 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:269d1854ac1a6add3bd4db55e5c54481f629c067b9e15512be69009d3eeb638c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222057948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10fcde7a95f16a6d448e4a51c700bf86a3c32ea8bed0669beafa8278b312274`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:13:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:13:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:13:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:13:31 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:14:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:14:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb51d1f6103c562773e5ad9b244bea0d905640ceeb1f8ac3e09c56a4396e5429`  
		Last Modified: Wed, 29 Apr 2026 23:14:06 GMT  
		Size: 126.7 MB (126652697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86294f53c691cd4b8219c4529be0c37d36eb392be9fc90e6ac8d50984f52706`  
		Last Modified: Wed, 29 Apr 2026 23:15:03 GMT  
		Size: 68.5 MB (68513044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de95a012ec478b1983275d908ab3c9ad3cd434ee11d8f3d677b0f81c991ace26`  
		Last Modified: Wed, 29 Apr 2026 23:15:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1596fc9c88b59ef47948192cc8377544f7b3db18d8248a49870e051191e995b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfef6c15e96931f985ae60d99ee2e842d67e13f3f90ec8ce9b1469159346f2b1`

```dockerfile
```

-	Layers:
	-	`sha256:c5937094a4d11a2b48790997f652842b33af21910c016b79b5a8678f63284575`  
		Last Modified: Wed, 29 Apr 2026 23:15:01 GMT  
		Size: 5.1 MB (5127635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496dc5c17e032e6908105a40379488fa7d8e418ea01f8d6fdbcc462a0bb53439`  
		Last Modified: Wed, 29 Apr 2026 23:15:01 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
