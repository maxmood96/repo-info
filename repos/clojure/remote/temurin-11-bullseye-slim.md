## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:a4477d44f4ea5fb464d1143253196db1ec4971080d07fb230293b326fd4e3ec2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:da47412259b0daaf7fd44f2dbfd952841722ed8ae140d2d41f297bff817210c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238243157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec4960718312724cea90ddf4aafaaf596be291e0f186f59ad329d9707116164`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03098f0d0fd1ec2940eb820cb7d8fe1170a3b2e52c0d5bda49530b007a858f1e`  
		Last Modified: Thu, 24 Oct 2024 01:59:45 GMT  
		Size: 145.6 MB (145601283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae18cad7d6e84537470c33cffc81e6fcd33c9c7e86df73e5801c52d0a89c275`  
		Last Modified: Thu, 24 Oct 2024 01:59:44 GMT  
		Size: 61.2 MB (61212430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71271fcb9e96cfad7ef2d5615dea2bace4d54a667530f68eeec2f3f4eae39ef0`  
		Last Modified: Thu, 24 Oct 2024 01:59:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:849c2d4b287332f93581d3ac92cec8ef08d265882aa67cbc82ab70321c6da214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b303a64e105f6bfd84e02c3aaceb15e9ead0901dfeba2b9474ddaa90013287fe`

```dockerfile
```

-	Layers:
	-	`sha256:7f1754b7a9d6f4c0048ef957b5393f113b5189fff3aa302d0c004cee75bd5e1e`  
		Last Modified: Thu, 24 Oct 2024 01:59:44 GMT  
		Size: 5.1 MB (5145487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db8487df8eb1f79db0bc1a6e64c8c1df732cd0b601743c41fda6064dafafc1f2`  
		Last Modified: Thu, 24 Oct 2024 01:59:43 GMT  
		Size: 14.1 KB (14144 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:db9d59d994b2353d47d4472bec6c7dd545f1753595ae3a326a211324da55d2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233762215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f8843eba6254b85983d01235ae155a5226e38394a1d8436bde803b970aab8f`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d15ddb0fe087446fc432cc41ac41015a1aaa06bd765a4885778025f96eacd6`  
		Last Modified: Thu, 24 Oct 2024 03:44:24 GMT  
		Size: 142.4 MB (142389106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979441870ceaff144a1da3d276d563b066ea40a9b975d1c58674d8e83a1733aa`  
		Last Modified: Thu, 24 Oct 2024 09:11:25 GMT  
		Size: 61.3 MB (61296709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d346b7b94b9125c7b4255190083bba49d2e464004da994e39bf903dbd25f9`  
		Last Modified: Thu, 24 Oct 2024 09:11:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:36e92cbf04667905ddbed64975dae8392db6364cd8aea06c0c2b7c0036b78c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154f8a5afe98d2278418d661cf579c7d35ce7e3d3a9e34546b92dddd2ab8e727`

```dockerfile
```

-	Layers:
	-	`sha256:4f0accf7059ee494d7823bdb9d0e2f7e8a191637993e87469cf28a56ad57a8e4`  
		Last Modified: Thu, 24 Oct 2024 09:11:24 GMT  
		Size: 5.2 MB (5151843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d57399c331be5de897c43c95d1544c6ebf9740127c0b04c33a243efaaa2a31ce`  
		Last Modified: Thu, 24 Oct 2024 09:11:23 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json
