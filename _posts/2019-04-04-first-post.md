---
title: "Welcome to Jekyll!"
date: 2017-10-20 08:26:28 -0400
categories: jekyll update
---
you will find something wrong

<pre><code>
package com.example.on.myapplication;

import android.content.Intent;
import android.support.annotation.Nullable;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;


/**
 * 출처 : https://blog.naver.com/eominsuk55/220222898504
 *
 *
 * 로그인 체크하기
 * https://blog.naver.com/eominsuk55/220228053631
 *
 */
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);


        Button btnLogin = (Button) findViewById(R.id.btn_login);
        btnLogin.setOnClickListener(new View.OnClickListener(){

            @Override
            public void onClick(View v) {

                EditText editId = (EditText)findViewById(R.id.edit_id);
                EditText editPassword = (EditText)findViewById(R.id.edit_password);

                Toast.makeText( MainActivity.this,"Make toast messeage ==> " + editId.getText(), Toast.LENGTH_SHORT).show();
            }
        });

    }

    public void onClick(View view) {

        Intent intent = new Intent(this, SubActivity.class);
        intent.putExtra("", "");
        startActivityForResult(intent, 0);
    }

    @Override
    protected void onActivityResult(int requestCode, int resultCode, @Nullable Intent data) {
        super.onActivityResult(requestCode, resultCode, data);
    }
}

</code></pre>
