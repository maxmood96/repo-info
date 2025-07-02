## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:8dab85b21ef7b8c8ece55d8bc8642814d4763d36b379df298d5b189916371b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:b99cc64cf8e2ed5b1b7b781469ed9f6eaf031967a354e36ee8b792786b15346d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124934666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72bf53228d79536ff63d7f9d4b5ce4b873548fbcfc2f5e9b6594b0027286347`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1599b0a98b85a8b18d2d5b3e72bacf9393ecd05db1f1b9cd33b32f4bc10fc4e`  
		Last Modified: Wed, 02 Jul 2025 03:11:24 GMT  
		Size: 6.7 MB (6664802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2004d045f49e4fa4bebd48ca9e88db2e7b98e155dbc155d3d3a727412eceea`  
		Last Modified: Wed, 02 Jul 2025 03:11:23 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeed148dd328cf83bfd42773d0106d61dcfdd9ffbb06888200e9f8140ba645fd`  
		Last Modified: Wed, 02 Jul 2025 03:11:35 GMT  
		Size: 88.5 MB (88547366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844ae8cbdf182305bf45ca47886cb89fa15ff44d3ad79e6c5681190f812f93dc`  
		Last Modified: Wed, 02 Jul 2025 03:11:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59736052dd0c5b82330aa78c411c32c182c5056b20f7cdc9fbdb8d7f5297a35d`  
		Last Modified: Wed, 02 Jul 2025 03:11:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:f2b02b42246543831d63ad37ed6230defd8a9a9ca170ff6df5b5213d466e18ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d737d4f2d418e4a2f0d7bb81823929abb5a7716894dabfa8b6014ab33f9b0701`

```dockerfile
```

-	Layers:
	-	`sha256:a1e879d77853f1d2c27e5ae1128f6031e8b9ca6b76bb122978c76d73ff1909ca`  
		Last Modified: Wed, 02 Jul 2025 08:20:36 GMT  
		Size: 2.3 MB (2311351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab96108efe38089b90d07e51c881a5e874e83721259d78f038c692eb6ded9918`  
		Last Modified: Wed, 02 Jul 2025 08:20:37 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:75f60c14d293ec57e956a07e68451e9d9af858618cca9e60231544f7bfbaa043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112220632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f453fd57ecc986077d41c8624247d5d31e330d3f945e8a753299a9f31d35cafc`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c0686a251b16fc8cbd211dd5bf5418ccc2bd75968ab247e18683ffb32d360e`  
		Last Modified: Wed, 02 Jul 2025 05:43:01 GMT  
		Size: 6.7 MB (6675401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929431d0f1ad953782d674eae05c259f14e0a696e1e97ac83b03b176f22ee189`  
		Last Modified: Wed, 02 Jul 2025 05:43:00 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e81089e3d5fc8f67c758495ca1c50e5a3b86124eee4dfa91353c312b6abb190`  
		Last Modified: Wed, 02 Jul 2025 05:43:31 GMT  
		Size: 76.7 MB (76685084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2330df6b859ca78ea65d96c83bed01eec6772a6b1f28b5f4ce9388e27d541ac3`  
		Last Modified: Wed, 02 Jul 2025 05:43:27 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9aa3d792e3a28e367667b7196477ea7a651af7579038fde794b2b043ba7324`  
		Last Modified: Wed, 02 Jul 2025 05:43:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:63cb39305eab924ce90286c15b7b146cc0b1b274856a08386e5e1c8cbd5b7fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33d2668880b2155ee2d001e05a69fae8c1f27524d42fe91fb18b10b539702af`

```dockerfile
```

-	Layers:
	-	`sha256:655564c624de9218821910a1f6bb4865b31753b439cef0c32cce71b4af32a4e0`  
		Last Modified: Wed, 02 Jul 2025 08:20:41 GMT  
		Size: 2.3 MB (2312433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b084e52b781825677e4f873a9e98ec32f92bff174b0966620bb5f5cb06d3eadc`  
		Last Modified: Wed, 02 Jul 2025 08:20:42 GMT  
		Size: 17.9 KB (17920 bytes)  
		MIME: application/vnd.in-toto+json
