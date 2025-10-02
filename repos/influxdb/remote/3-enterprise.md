## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:c75021ba18b0a86551b10593331b5606c16f778f3ae495b6f2212a4105ea3ff7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6c51e7d7440be393d65bacf11e1475b5d18ea68f19640aa48c8485bd1aa3d94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125829821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5624966dcf7c1d8813234fa587718f0a18345e13574a7319f6450500061ec8e5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58135b4742ad7ab7fde2d84ac35ffb70c4460efcece64c99429ab49fbfde1848`  
		Last Modified: Thu, 02 Oct 2025 05:09:01 GMT  
		Size: 9.1 MB (9070624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b822677ce7149474eb17d8b2bb719ab134b57dc258ac28e7306639e322d269f4`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6993110cfe96002dbe82f2970c92edeec13e4f3227d6d821c6ac05161b123eff`  
		Last Modified: Thu, 02 Oct 2025 05:09:07 GMT  
		Size: 87.0 MB (87032058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70c1dfab21ede393803c044cc98a552bae418dfe27a39434ccb11ac7c793420`  
		Last Modified: Thu, 02 Oct 2025 05:08:59 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852f3b98ef80c7ea583046ae0d2dff3a56afba76a621d57bc49c3ec7a2d18c18`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:2fd31cf487e3fa050feccb33daeafe7214c7e7c9da14f4a339bdc089cd947aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93dd7daeaf1bf16b43f23383d596816c3baa6adda8529774e61109568bf2a61f`

```dockerfile
```

-	Layers:
	-	`sha256:9a5906f2fb7d99e5a8b020d96e38421ddd6d1a0a8a9e93031bddc3bec9360d31`  
		Last Modified: Thu, 02 Oct 2025 08:20:34 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cbc20234791326927d74160ca6f5990c4e0e7834323da0032987cbadb671078`  
		Last Modified: Thu, 02 Oct 2025 08:20:35 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4b65e4afa4793137b88565448d1c4b421a78dd4d9b88f052b4560f0de22ce84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116158253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090eb66a46758bb21e05ee0d374d333985b93c0d41ab42ebadb954f79283e7c5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae1910013bf0e361618c72b829e50d3bbdaacb3ef7f87236a7b6704f1a5d39`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 8.9 MB (8892549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d81e6ff420e726466d2e0e6c3f592d6f07918ddbdbec4c3a2cb6bd912cab10`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcdaf2322d4771576222f45e766fe939f261778899a002599e6de2449ba6929`  
		Last Modified: Thu, 02 Oct 2025 01:24:21 GMT  
		Size: 78.4 MB (78400002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff341ebda249e4011610f56e3403de7087b365c184af05a201d8ed7ca79668f5`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e955fdcba3a0d5795d6109eb17c028c1c3380f4e578b7ede2a271364d14638`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4f68f62fb9ee3f9c0aeb74d6a20afb0b056ead3a0f2685bacbd9e172d4887ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838b58787ab46cb6649eb50a038f2a0aea9fe89998d8f69a040e720f7c231bdd`

```dockerfile
```

-	Layers:
	-	`sha256:bf5b4a9c0694efeb04c36c74cfca0ef3ab0354cf22b8b25791734a26d57ba905`  
		Last Modified: Thu, 02 Oct 2025 05:20:38 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01911d86f39a79e1ad18970ad82c646ab57e02b41ea0191902d18e773758793`  
		Last Modified: Thu, 02 Oct 2025 05:20:41 GMT  
		Size: 17.9 KB (17920 bytes)  
		MIME: application/vnd.in-toto+json
