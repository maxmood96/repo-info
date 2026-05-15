## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:1d48ea4091523254bf98a5fa0bf06ad70c1245e71ec3e2e2068471f52c3542d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c397147caef0afc05dece93222d0dd3f733c8a6ebf8b42522bfa13da2be5136b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235335328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84374a57719f4419d62ac07d25550062f34b005dc16e7e38ae05a1a85f3ef0de`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:13:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:54 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:55 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667524d0ca77fb230742fd3efe85aa608b7d998417bf838fb65e39d61f118210`  
		Last Modified: Fri, 15 May 2026 20:14:31 GMT  
		Size: 145.9 MB (145886262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9382ff95ee3c8e43eb5d73842fd51b164d3ab4fb2bb27953eee6425c53d5dede`  
		Last Modified: Fri, 15 May 2026 20:14:29 GMT  
		Size: 59.2 MB (59190462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8530107a0a6b3395ae42c32699ae01163bc5282b295e110308a321fffc467c73`  
		Last Modified: Fri, 15 May 2026 20:14:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:044a8a628b98402f7e68fd343901b28ac17018ae2362995b8bc5fff8c05dd35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7b411732564014ffdaf05cd5722dfe08f01a586c58c549ee24ecb30fdc726`

```dockerfile
```

-	Layers:
	-	`sha256:e40812395294e026e1830a4f003f113932cb9519c70e5735066de1924ba1f93b`  
		Last Modified: Fri, 15 May 2026 20:14:27 GMT  
		Size: 5.3 MB (5340194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88049096e8a517243554c7dc77aff1ba2f345c03b323c528c752a4045bacdadd`  
		Last Modified: Fri, 15 May 2026 20:14:26 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fbfb70c46fe61198b8100910a2553f98042615d78f76e5eba4956b8b097ff61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230685259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85180513fd1634082315d853a1689db1aabb53469354543d47bb26c605ab2b6a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:13:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:51 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:51 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2616ffd297f04748f9d197f017d1e7bcd66190b934922696445bba17a903c3ad`  
		Last Modified: Fri, 15 May 2026 20:14:26 GMT  
		Size: 142.6 MB (142582236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4f560ee90da628eaea14c49d0019ba36d3e71976c75f045bf33645a1b6a88b`  
		Last Modified: Fri, 15 May 2026 20:14:25 GMT  
		Size: 59.4 MB (59359786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11a7381eb4f729e9ed5c7380cba0ddbfed8cbadaa0474102370ae7bb8af6e0d`  
		Last Modified: Fri, 15 May 2026 20:14:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c4b117bf5cf00d993fa5e06d84d1fbc3aaef879233fd87de940344b52b94a020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03af3421be6fb18f4d10449a874efebfefba773fbe472811362eca930c55c9f9`

```dockerfile
```

-	Layers:
	-	`sha256:08533ec53dad6412846e7e56cd75fd98e5d188343ccef3ea4e44b82947f6e9e2`  
		Last Modified: Fri, 15 May 2026 20:14:22 GMT  
		Size: 5.3 MB (5346544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb3f4c30a7ce106ef3555375bf0077e10dfb491142b34a65fe1ee1c9dac7abc`  
		Last Modified: Fri, 15 May 2026 20:14:22 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json
