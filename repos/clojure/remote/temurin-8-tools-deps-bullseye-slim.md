## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:750efef0e32daea7573a76ddb6f50be888b6db64ae42a4e3a45772db13bb685e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e71a16275faadd13b17afa11458da1c761a0204a43f88dab5110b5b3b485e92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193981292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678334f08187181d58c77a3fda86c81bb91810c182d599826c0fc13548c90739`
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
	-	`sha256:58d8ce46e06609fbeb67fa542d703751b00fe6344a35ba9dfa19098da6848e3a`  
		Last Modified: Thu, 17 Oct 2024 01:13:25 GMT  
		Size: 103.6 MB (103611899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343a8dc739be18a71cd715b1b823e770f3ea801709ba2f36c8db2c44d75d0b68`  
		Last Modified: Thu, 17 Oct 2024 01:13:24 GMT  
		Size: 58.9 MB (58939951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6777e6103741036b7f71e1c15321adc21404612b6c5ff2cae783c0444a25ff`  
		Last Modified: Thu, 17 Oct 2024 01:13:23 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:49e6c35e990d75bf27667e73905487dd283aaa4f442481e986b969372100e41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d556bfbb4c8c9319b8020d7b826f0b6dc7d4f73ac003266841ebcf2ed15fc878`

```dockerfile
```

-	Layers:
	-	`sha256:67635ae00ce98a1fbaad0a64df845dd20a861450de72abaa557662089e87bed5`  
		Last Modified: Thu, 17 Oct 2024 01:13:23 GMT  
		Size: 5.2 MB (5221741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaf17fdf7e36420db492506b8cc7248e6eb955f2fe08298c86eb625b7daeeba`  
		Last Modified: Thu, 17 Oct 2024 01:13:23 GMT  
		Size: 14.0 KB (13959 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:51797b2ac97c85d978835dac267df666ae01d753f058cf38c0e27f6f503bba6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191879099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f29fa31d8e19d014d2660e3d8f3bf8e6359cef0be53a39aee5ce66443a0aa1`
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
	-	`sha256:feaffa0bcbc7a9d9358c92cae47bf60b7dc6453e4dcd0145711896cdaf0ce32b`  
		Last Modified: Thu, 17 Oct 2024 07:58:37 GMT  
		Size: 102.7 MB (102729275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80590cf294636247a1b4f9469377aa29914530305abcd62558b3cccd7482f820`  
		Last Modified: Thu, 17 Oct 2024 08:02:29 GMT  
		Size: 59.1 MB (59073423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084241ce2d21116ddb6703f7e3d3cfab140bcf464f9cb0d23ad893d8a1b9e9c4`  
		Last Modified: Thu, 17 Oct 2024 08:02:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ac3b67db0b8eda9af955755e0f34700fe2b730aa463143a9c9fd8c840a1a58a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fed442581f585837f06fd21f57eda8d2ff1fc2bd9c500b91f7da97a71cf707`

```dockerfile
```

-	Layers:
	-	`sha256:4b42a6ee5d06c203f85dc4392bb5dabb17024cb95835e8adc7a61804d23f702f`  
		Last Modified: Thu, 17 Oct 2024 08:02:27 GMT  
		Size: 5.2 MB (5228177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de28e30eec7e4291d770e95eb2857e3836aed20f2080dce875ffb591fce57743`  
		Last Modified: Thu, 17 Oct 2024 08:02:27 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json
