## `openjdk:27-ea-jdk`

```console
$ docker pull openjdk@sha256:65ade9383c577595402f9859f56eb4e5e3cb9dc00852472bb192640550800176
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:5fa49ed9fe140177e38cb0598252a283c6f07f89d5d14c5a3fa9cd761a300374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314024269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe78506e7e88b5455a3d6b56510f69b574a2a4a4ee01fd426f6b883b1574d594`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Sat, 07 Mar 2026 00:40:23 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 07 Mar 2026 00:40:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 07 Mar 2026 00:40:35 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:40:35 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:40:35 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:40:35 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:40:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb41a59e5e559a42f15aeabd32c6a462c54e0369088e60aca7fc2143a93b2d5`  
		Last Modified: Sat, 07 Mar 2026 00:40:57 GMT  
		Size: 38.3 MB (38298183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d12f82cd3431fa9181c78c26a20a7e8b9033c6ec6714c33e0459c030b319b6`  
		Last Modified: Sat, 07 Mar 2026 00:41:01 GMT  
		Size: 228.4 MB (228417215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:c5b15b91b5f309d3fac77427fc805fff36ee8429a75d35ccfb40749cb6643887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f35262da8e9fb9603d91be976819e5896745e249aa94558baa1ab278a0bee3`

```dockerfile
```

-	Layers:
	-	`sha256:be0b66c641b15b257e5e95563e760caef9d8c188dfc9c7d6a0cee2e74045d870`  
		Last Modified: Sat, 07 Mar 2026 00:40:56 GMT  
		Size: 3.7 MB (3655437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d25825c73d70ee273b3cd9fe13043d48330a95f82b243c1cb5922e2e2735023`  
		Last Modified: Sat, 07 Mar 2026 00:40:55 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6f2fc6c2332c7405b26712046cd598df9284dcb24621a12a811c9ff8c7f0234e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (310962854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08a1b270ea51dc2b556ab57fe3667618d25806184c8b5b32ecea86146814e84`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Sat, 07 Mar 2026 00:41:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 07 Mar 2026 00:41:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 07 Mar 2026 00:41:40 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:41:40 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:41:40 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:41:40 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:41:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0929214c9f6a7b2f3c00ee2603eb15c65b8fd4adb34f8c106c07ea110bea9f33`  
		Last Modified: Sat, 07 Mar 2026 00:42:03 GMT  
		Size: 38.7 MB (38693755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65120397d49ce4edcb0a6affcd9d50b696d0c00b1ee5a48654a77a32330d2493`  
		Last Modified: Sat, 07 Mar 2026 00:42:08 GMT  
		Size: 226.4 MB (226367119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:4828d53b7606211ff485356d926a68821530f8b656dacb5f84b8130a78780908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867f8b6d20c45d3c384452b18f106339b319887e99704610eabf33229701ad00`

```dockerfile
```

-	Layers:
	-	`sha256:4599c6813516b2e8a7df3039da8f6000a29418976dbf171717f4d06d33ed74d9`  
		Last Modified: Sat, 07 Mar 2026 00:42:01 GMT  
		Size: 3.7 MB (3653127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca745f01c9110dcdedbec97b345189bc448c6536b6798a2acd4bdd5a07c84e7`  
		Last Modified: Sat, 07 Mar 2026 00:42:01 GMT  
		Size: 18.1 KB (18051 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:1a7a5f9c60e75ff10997b2da2717892b2f63f9ca5e9cf6a823bc5467a24ab923
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190272988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e59f7667eb96998f06b3851d28ce03d5103fdfc86a453cea8cc62e206b5658`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Sat, 07 Mar 2026 00:42:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 07 Mar 2026 00:42:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 07 Mar 2026 00:42:44 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 07 Mar 2026 00:42:49 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 07 Mar 2026 00:42:50 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:42:50 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_windows-x64_bin.zip
# Sat, 07 Mar 2026 00:42:51 GMT
ENV JAVA_SHA256=bb5331abf59ac46c0dd11cefa00cc052f8d7cf6384d850b919591cb3346acbe4
# Sat, 07 Mar 2026 00:44:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 07 Mar 2026 00:44:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cd68618a3981d21fc71c8d5f0a7768e0e9644aa80ed89bcf74e77c5eee17be`  
		Last Modified: Sat, 07 Mar 2026 00:44:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127b9488130912dd6a0c1b707ba527f35a87bed52b80ed945ef9ed12c9dba58`  
		Last Modified: Sat, 07 Mar 2026 00:44:16 GMT  
		Size: 392.1 KB (392125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f608afcdd2d523a3c719ae2acc3b310bf6f749e12a88385bc231704250d4bb`  
		Last Modified: Sat, 07 Mar 2026 00:44:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d92d62a6660e8272501121839c0da8c6c60c9ed3ff5873f938bf5b063e1075b`  
		Last Modified: Sat, 07 Mar 2026 00:44:16 GMT  
		Size: 375.2 KB (375245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a9bf21fedf8b8eba8e36cef4846ce93ff5ea18136b51d611ad048c79b89d1`  
		Last Modified: Sat, 07 Mar 2026 00:44:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9cf6bc963ff9b07424c6f04d7ed9a931bbe46357e3ed6c70fcc77e38e951b5`  
		Last Modified: Sat, 07 Mar 2026 00:44:14 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccc362572994618df6647e7ab9947a4c861436bfd2cebbf961ad430bb97fbce`  
		Last Modified: Sat, 07 Mar 2026 00:44:14 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd521c0a9f3cb3757471932f2ca1692aa2fafd970483cec36da92bbb6f38720`  
		Last Modified: Sat, 07 Mar 2026 00:44:30 GMT  
		Size: 224.7 MB (224737932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b763d2ef552130d77e6a22004ff9fcdfe56c3bb90306be1c43234a3ab202dd1b`  
		Last Modified: Sat, 07 Mar 2026 00:44:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:659be96f4b08263e91fbdffe619c61b6cfb3fa2c7e20cbf823641e41da2375b6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088264222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6914f939873051b3b4185fc30ee9b4814381612c4b31020f80da867841b723a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Sat, 07 Mar 2026 00:43:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 07 Mar 2026 00:43:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 07 Mar 2026 00:43:43 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 07 Mar 2026 00:43:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 07 Mar 2026 00:43:52 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:43:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_windows-x64_bin.zip
# Sat, 07 Mar 2026 00:43:53 GMT
ENV JAVA_SHA256=bb5331abf59ac46c0dd11cefa00cc052f8d7cf6384d850b919591cb3346acbe4
# Sat, 07 Mar 2026 00:45:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 07 Mar 2026 00:45:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6e8dba04deb4778bb53227d2f2b7d36d3ec9dbd6c229dae635f7a1ef347b4f`  
		Last Modified: Sat, 07 Mar 2026 00:45:25 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816998ede68709017432c727cfadb1218e0b2f6fec64343c3bc4132edcf9db7a`  
		Last Modified: Sat, 07 Mar 2026 00:45:25 GMT  
		Size: 511.2 KB (511199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92907900c89948b025f256bbc02c99f5a70461413ef8209fbd86f5a02ed50dad`  
		Last Modified: Sat, 07 Mar 2026 00:45:24 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8204cc39f72950db2a0b24e0aa9f22c94fd32d0e2340acefdc34b3bd8063b6`  
		Last Modified: Sat, 07 Mar 2026 00:45:25 GMT  
		Size: 350.1 KB (350099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f0899f472cfaa750c1590d8ff62ad552400c15585284b11f4ce4cec550189`  
		Last Modified: Sat, 07 Mar 2026 00:45:23 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d2ce9d9fe41b7f5892c89a27f75609a55a464c89e8c607d43438adabb76308`  
		Last Modified: Sat, 07 Mar 2026 00:45:23 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31e5ddfe67002e1307e64a9d2f9abd276d1983c7c5b31ca56f1699a2442bc74`  
		Last Modified: Sat, 07 Mar 2026 00:45:23 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47334ad792e6a1e14c9ad824e9821985935433f97d1db0e229a8525ba12e032b`  
		Last Modified: Sat, 07 Mar 2026 00:45:39 GMT  
		Size: 224.7 MB (224737832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65da38bd43be05c70506d0c895a02e43b074196bb198f2619da21a9e31520a3`  
		Last Modified: Sat, 07 Mar 2026 00:45:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
