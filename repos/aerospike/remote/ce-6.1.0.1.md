## `aerospike:ce-6.1.0.1`

```console
$ docker pull aerospike@sha256:24be5c325986e4c977b0966fc98b8420542f01c84e6cde2dec956ca02d661c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.1.0.1` - linux; amd64

```console
$ docker pull aerospike@sha256:ef52a9b0dc4dcdce3e46766310fb4d657bc9d35235d111f92f452ba554e7aa61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121425094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e75661cbc762dc66176cccf68f6fae6de51eb0e6e85667e1a74237694d1afd`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:39:11 GMT
ENV AEROSPIKE_VERSION=6.1.0.1
# Tue, 13 Sep 2022 03:39:39 GMT
ENV AEROSPIKE_SHA256=e100c35ce9b42bf1daebf668f134de444dfc3f6fcef60479f1e9469d9761e791
# Tue, 13 Sep 2022 03:40:00 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && if [ -d '/opt/aerospike/bin/asadm' ];   then   mv /opt/aerospike/bin/asadm /usr/lib/;   ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f /usr/lib/asadm/asinfo ];     then     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;     fi   fi   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 13 Sep 2022 03:40:01 GMT
COPY file:f497c4c6974a190f79a562efd9c9c0d6b753efe43e62c3fcc2536f74ad08238d in /etc/aerospike/aerospike.template.conf 
# Tue, 13 Sep 2022 03:40:01 GMT
COPY file:fe302e12e47afe1731a34ed4ed29328c6901a3f2c9e32e307220e65cb76d53a2 in /entrypoint.sh 
# Tue, 13 Sep 2022 03:40:01 GMT
EXPOSE 3000 3001 3002
# Tue, 13 Sep 2022 03:40:01 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 13 Sep 2022 03:40:01 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1294495bb1c5f96dcff79bc25629d6ac5f86211c3d08c389f88f6e917b797cd9`  
		Last Modified: Tue, 13 Sep 2022 03:40:49 GMT  
		Size: 94.3 MB (94292710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d2db41bf36d7d4c29edfaa1898c2534a988e5c6b94a938d23457ea63a15df7`  
		Last Modified: Tue, 13 Sep 2022 03:40:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5e63c522e8b05c0f8130c70c57bf69479e2f09efd2f9561ddcc9d107bf9054`  
		Last Modified: Tue, 13 Sep 2022 03:40:35 GMT  
		Size: 811.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
