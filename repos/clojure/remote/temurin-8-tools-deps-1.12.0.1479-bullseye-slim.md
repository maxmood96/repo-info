## `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:c87804d4b8c94d58de92b5333a2339a0b26b7bc0c33395d979dd1df032be3f25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e10bf150b103738bfc9b3d1eb1afefc33577e99f120a760e7c978a964846f784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196275330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3409e34bc7b33e872656a6a8d6431978e15f0bcb7d1274cb6700431dc4165540`
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
	-	`sha256:06921a40bdb086f9b6663150f7e6b79963339dc71fe4bed0c995e59e475db78d`  
		Last Modified: Thu, 24 Oct 2024 01:59:09 GMT  
		Size: 103.6 MB (103633964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c77c3abadb836a3271684f28d175977b8b6adf80f3d3f9445993853bd1732c6`  
		Last Modified: Thu, 24 Oct 2024 01:59:08 GMT  
		Size: 61.2 MB (61211921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d0795e43173b3b6bf275bcfb9568393cf24e5a75ba843fbe0d17e6c3a4fac4`  
		Last Modified: Thu, 24 Oct 2024 01:59:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b7c8f24c393b90dfebc9f287d68f4a4e22d364d3f42f1398a60139c6973f3df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5261616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed9271d98be9a03a03f9504481de37fb5524c041c83f11b688e087a8e1f0a3d`

```dockerfile
```

-	Layers:
	-	`sha256:438660b0abb443626f01126799e852ac8184438db142fd90ec48a86ef7e742c1`  
		Last Modified: Thu, 24 Oct 2024 01:59:07 GMT  
		Size: 5.2 MB (5247486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86680dc19d97603a5ef6021e3e756cca896be53ef52ff7e7ab11ca7a8696f7e`  
		Last Modified: Thu, 24 Oct 2024 01:59:07 GMT  
		Size: 14.1 KB (14130 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a835188a700591a4e3ccbff12eee87343ebbb8c9b97f30ab8a6e3bb3506a6e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3a65eb3e7136c8f17252987b14068c0ef7eda70c81c629e742bfac5454b4c3`

```dockerfile
```

-	Layers:
	-	`sha256:eb5adcfc5183ddb1844b4a2941eaa51afcf79397b091b0dcfb6f10dfe609809a`  
		Last Modified: Sat, 19 Oct 2024 11:45:45 GMT  
		Size: 5.3 MB (5253922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e149b3f3dd31444955c879025d99cb9be3eb557b42faadafc5d18ea44366c3`  
		Last Modified: Sat, 19 Oct 2024 11:45:44 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json
