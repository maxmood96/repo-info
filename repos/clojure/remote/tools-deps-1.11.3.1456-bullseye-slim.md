## `clojure:tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:6b81e48f1ae66a1daa407aa8215a5b2826f1fbd0898b3064c8a103e31657029d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c39a11528cc32914dd14e53b8cbbc61929fc844d3f4a997c617ca14eccf2ef80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248545562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee4d06ebf86dce8933e0554b40a23e2f49f79940185eac9d975e324b7a27ccb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4df991dccd20ba9d65b13413906da9d835edb65ab6820acc607282fa0e1f7b`  
		Last Modified: Tue, 02 Jul 2024 03:03:00 GMT  
		Size: 158.5 MB (158497942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b467ef1dbeb128b3f62b93318c83febffaed5d3e811a9a0434815080211ce449`  
		Last Modified: Tue, 02 Jul 2024 03:02:59 GMT  
		Size: 58.6 MB (58624295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f3dbcdb7a96644a6540701dd7412e358afdb66cabc946c157891e9cd09a243`  
		Last Modified: Tue, 02 Jul 2024 03:02:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e230618837080244f3060611e495dae42ac036c7e61a25da8315dcc02336a638`  
		Last Modified: Tue, 02 Jul 2024 03:02:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa3b52d1e175d39192e1029a522c375b87358238c367022da282eef7b0101d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecdf221eb454914684b4b9ddcfd9998fa82ce9f89bb290aedf7e68665ab7f9e`

```dockerfile
```

-	Layers:
	-	`sha256:4314a5098be5611b739ea559b7588445a3e8aa28644b35d25463a64ed0d3eacb`  
		Last Modified: Tue, 02 Jul 2024 03:02:58 GMT  
		Size: 4.9 MB (4909978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eca983c71c6ccf4993b9ad0020fa10dd8c52fe83b8002fe966690e31be92317`  
		Last Modified: Tue, 02 Jul 2024 03:02:58 GMT  
		Size: 16.2 KB (16207 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:476af18ec09dde10cce2c8bdf1d90306b1b922e3097ad10b8e14eb767af4211f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245293715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489d45e8b12e0effffedff9ba5b1f155fc0dfee5681e02bc2d7061fb0156fc17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564c25575a74b32dc66c660031ab1490f376022bf7649dbc787565d8d624ecc`  
		Last Modified: Thu, 13 Jun 2024 11:55:25 GMT  
		Size: 156.7 MB (156665603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4395531b57b9297e6482780146a12ee3e43b0756801083f18dc44dde387bf7`  
		Last Modified: Thu, 13 Jun 2024 11:58:39 GMT  
		Size: 58.5 MB (58540090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7df60427849291e07912f0b4d52e0c6ab918ccbec5920db164d777663f03714`  
		Last Modified: Thu, 13 Jun 2024 11:58:37 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9142cd0cd47e66744a097f3cbfffe000be70f82efc865d9ee44042de74174ba0`  
		Last Modified: Thu, 13 Jun 2024 11:58:37 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4380d255625e1c9e7abaee2689d4eaa69745cabc3bee02f57e58c967bb8ef84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9049262c6963c2e659c1ac5c0d91f91c8885648224353083bef943e29c22c73a`

```dockerfile
```

-	Layers:
	-	`sha256:ef2a1283ab590db748cafd4e6b22ce30bd29ddf3cec6ca18ccad7568e6219867`  
		Last Modified: Thu, 13 Jun 2024 11:58:38 GMT  
		Size: 4.9 MB (4916319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c01cfff1e4abd4c093be53a99c139bd5130c0fff82c969eae73c11304cfb55`  
		Last Modified: Thu, 13 Jun 2024 11:58:37 GMT  
		Size: 16.8 KB (16773 bytes)  
		MIME: application/vnd.in-toto+json
