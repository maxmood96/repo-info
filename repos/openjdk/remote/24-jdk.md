## `openjdk:24-jdk`

```console
$ docker pull openjdk@sha256:bb7a30977811c4ed2d21307230ca0066f26366d94513c037ab76f0bbb4351b5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `openjdk:24-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:b008bd2eb168964aeb50701850d50da055fa8ba1ce5239bfaf58ec084dde8be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301518849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb3e19ea5f2c0b9accede63d3ff74b8910736ef42b971914a612dc1c2b36b86`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 20:34:59 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:34:59 GMT
CMD ["/bin/bash"]
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 14 Sep 2024 06:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Sep 2024 06:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_VERSION=24-ea+15
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='b41d4867c348d7f1991085d8bcc8797eaf032d9dfaa3419bc9db15eaea75e91e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='165b7c19403e9708ca261cdfe4c385e837df683049203e33ad2bf76228054a25'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5e407bf3af905fb1f6edf271f870052697e79b018f921119921615cd25365fdb`  
		Last Modified: Tue, 10 Sep 2024 01:02:42 GMT  
		Size: 49.2 MB (49239252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b827a6775178595a4e839f335fb59d678dace1d642b33f76e68550f367346f6`  
		Last Modified: Mon, 16 Sep 2024 18:58:02 GMT  
		Size: 40.4 MB (40417947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fb5533ac77b9dca88397e870dfc5032b19a0478d14ea72b95dfe64dbfba361`  
		Last Modified: Mon, 16 Sep 2024 18:58:05 GMT  
		Size: 211.9 MB (211861650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:c42f882692a731764cad821c83d01624ed013032860e6213c3e6c4a68a3165d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602333ce284b5c82c5e16a1892ec8d83002cce9906404a10e073168a74d5773e`

```dockerfile
```

-	Layers:
	-	`sha256:030c526d3d5041c535b9a5d454a9626f2b10776311bf96094558023dd48aba67`  
		Last Modified: Mon, 16 Sep 2024 18:58:02 GMT  
		Size: 3.7 MB (3670499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef8978d8b8406e1d7586d39234697e856c03f6d1cb5d4784c32d4e8137bb57a`  
		Last Modified: Mon, 16 Sep 2024 18:58:01 GMT  
		Size: 19.7 KB (19712 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0afe7650e2f8684027697bf700a88d8b25bbc4a13b2eab4a92847e824ba0369e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298459256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932595dcdca2fa82451b07ef6f6c184472adbc2762a0692d0b8b66978be874fa`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 20:35:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:35:51 GMT
CMD ["/bin/bash"]
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 14 Sep 2024 06:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Sep 2024 06:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_VERSION=24-ea+15
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='b41d4867c348d7f1991085d8bcc8797eaf032d9dfaa3419bc9db15eaea75e91e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='165b7c19403e9708ca261cdfe4c385e837df683049203e33ad2bf76228054a25'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed6a7145c00ee1c4b91b6b37765e2a7addef2d9b96e12546b2f7aad0a198ae3f`  
		Last Modified: Tue, 10 Sep 2024 05:32:56 GMT  
		Size: 47.9 MB (47913808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1be39ea2d18e49c60b19f004c35d6d158839de1ab591a32c52003cd6b2d1b9`  
		Last Modified: Mon, 16 Sep 2024 19:19:57 GMT  
		Size: 40.8 MB (40844107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ec9a476755f71cee55be483721187d841ffbacd3182c203e191653ab5b1e42`  
		Last Modified: Mon, 16 Sep 2024 19:20:01 GMT  
		Size: 209.7 MB (209701341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:5b60fe9f7b6229adffc04af0cbd3ba5190da434f78ef5c11d31f454b68f8b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c952c44eb24f06febb690fc364f91618199a5f455db3b266b064573fb5fdc501`

```dockerfile
```

-	Layers:
	-	`sha256:71709746f2934aa607286bc77b4576cb86db69b10530ff00c7fdea984a957518`  
		Last Modified: Mon, 16 Sep 2024 19:19:56 GMT  
		Size: 3.7 MB (3668882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b398419c6233f373563ce4516dc49a2e0ad6ea586e2c31c255e3c6e37f366ec2`  
		Last Modified: Mon, 16 Sep 2024 19:19:56 GMT  
		Size: 20.3 KB (20265 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - windows version 10.0.20348.2700; amd64

```console
$ docker pull openjdk@sha256:6eb4d7e75f5b56e229856843d35c6e5cc3055baab1a10d5901e2cfce18cc1a86
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1670896015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea72dded6c19883841917d8676d99e5dbb436094d7d17dfc477ee442cd00f6b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Mon, 16 Sep 2024 18:57:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Sep 2024 18:58:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Sep 2024 18:58:34 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 16 Sep 2024 18:58:40 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Sep 2024 18:58:40 GMT
ENV JAVA_VERSION=24-ea+15
# Mon, 16 Sep 2024 18:58:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_windows-x64_bin.zip
# Mon, 16 Sep 2024 18:58:41 GMT
ENV JAVA_SHA256=eef80af228bec40c318932471d2263a3ee6998dd635f9b1e60c432cf26d3c4d8
# Mon, 16 Sep 2024 18:59:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Sep 2024 18:59:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ef27b6c8090f6896371ec9eb5543810593416ba4a510b64b2eee9e5f2ebdaa`  
		Last Modified: Mon, 16 Sep 2024 18:59:10 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60161ef3c2f2a60ac39f5b92de51569642e97199b5a82580631124b8440d7fff`  
		Last Modified: Mon, 16 Sep 2024 18:59:10 GMT  
		Size: 350.7 KB (350735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a9cd75456157cf6f64693370e20beae84aa2d2414fe4d0da7874ceb5b76e50`  
		Last Modified: Mon, 16 Sep 2024 18:59:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0712c6b05d28296383a953360b19b27876c74d96eba90f9685168a7f1cea1c57`  
		Last Modified: Mon, 16 Sep 2024 18:59:10 GMT  
		Size: 334.7 KB (334704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765cd56241300bdbd1bd204600b9941e0db4372912a950d43155433164223f5e`  
		Last Modified: Mon, 16 Sep 2024 18:59:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246207d39f6867729bafd5939410b2f370576368899e99e2ce7a2f51faf89bef`  
		Last Modified: Mon, 16 Sep 2024 18:59:08 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43e18eb5e0ccba6e7f868a21577575da44a1bd33fa0a2bc5d5fd17a9c807807`  
		Last Modified: Mon, 16 Sep 2024 18:59:08 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3b21c60f129547a3f5a603f3c6106b4462f92c550556b55e769f33036d6ab9`  
		Last Modified: Mon, 16 Sep 2024 18:59:20 GMT  
		Size: 208.0 MB (208010462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ac0988e4a96de417d28e670d9d14d3557e0aec57591c1f953e5307c514ffa0`  
		Last Modified: Mon, 16 Sep 2024 18:59:08 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-jdk` - windows version 10.0.17763.6293; amd64

```console
$ docker pull openjdk@sha256:b7ab4d30c27e52192d41ea30dc4e2aa288f92f97674d59c3c76122887153930a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1929012901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb56a222ae9b8e3e9de2c499e9d1953caa5586164acb6195842da58070f61a6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Mon, 16 Sep 2024 19:01:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Sep 2024 19:02:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Sep 2024 19:02:06 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 16 Sep 2024 19:02:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Sep 2024 19:02:16 GMT
ENV JAVA_VERSION=24-ea+15
# Mon, 16 Sep 2024 19:02:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_windows-x64_bin.zip
# Mon, 16 Sep 2024 19:02:18 GMT
ENV JAVA_SHA256=eef80af228bec40c318932471d2263a3ee6998dd635f9b1e60c432cf26d3c4d8
# Mon, 16 Sep 2024 19:03:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Sep 2024 19:03:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d23a5fee49056fbcd1f2a4d97695710988c3fcb29fcbfd1b3a49d77c118a9a`  
		Last Modified: Mon, 16 Sep 2024 19:03:10 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a02190921c086f94550f4de47987a7fbbf6dd32495c8779d03f381a2370f49`  
		Last Modified: Mon, 16 Sep 2024 19:03:10 GMT  
		Size: 352.4 KB (352403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238c1b16b9e779a9d5ddc29ed93b8600675b5f07865171ca08dec9c87f23bd28`  
		Last Modified: Mon, 16 Sep 2024 19:03:09 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f59605927960401d079ec173530abb5e93dcb163095b2f6d73d4c4d62290fef`  
		Last Modified: Mon, 16 Sep 2024 19:03:09 GMT  
		Size: 345.1 KB (345106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92dbe9a9f2222bc2c90a9aeeeeb9f4b9ce2a35e029abc3ff17397d9e0a2a29b1`  
		Last Modified: Mon, 16 Sep 2024 19:03:07 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7f5b542f993e99158129da9b95f14e01088fccbb2597f9b9c169a52f4539d5`  
		Last Modified: Mon, 16 Sep 2024 19:03:08 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fc8124b392aa6942a88e2899696258487e32a6ad519f5f9690e10665363e78`  
		Last Modified: Mon, 16 Sep 2024 19:03:08 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4601edd11f2cd28b0442fcd9ce57670e502937c8777c522c537496952b6d71`  
		Last Modified: Mon, 16 Sep 2024 19:03:19 GMT  
		Size: 208.0 MB (208038994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1925be6f5f865480b69219ecc4c5eba4d22de52acaea71de78d6caa935dad9b7`  
		Last Modified: Mon, 16 Sep 2024 19:03:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
