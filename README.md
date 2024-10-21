package com.example.portfolio

import android.content.Intent
import android.os.Bundle
import android.view.Menu
import android.view.MenuItem
import android.widget.Button
import android.widget.Toast
import androidx.activity.enableEdgeToEdge
import androidx.appcompat.app.AppCompatActivity
import androidx.appcompat.widget.Toolbar
import androidx.core.view.ViewCompat
import androidx.core.view.WindowInsetsCompat

class portfolio2 : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        enableEdgeToEdge()
        setContentView(R.layout.activity_portfolio2)
        val skill = findViewById<Button>(R.id.button)
        var t: Toolbar = findViewById(R.id.toolbar)
        setSupportActionBar(t)
        skill.setOnClickListener {

            intent = Intent(this , skillsActivity::class.java)
            startActivity(intent)
        }

    }


    override fun onCreateOptionsMenu(menu: Menu?): Boolean {
        menuInflater.inflate(R.menu.main_menu, menu)
        return true
    }

    override fun onOptionsItemSelected(item: MenuItem): Boolean {
        return when(item.itemId){
            R.id.i1 -> {
                Toast.makeText(this, "Refresh Clicked" , Toast.LENGTH_SHORT).show()
                true
            }
            R.id.i2 -> {
                Toast.makeText(this , "Exiting App" , Toast.LENGTH_SHORT).show()
                true
            }
            else->super.onOptionsItemSelected(item)
        }
    }


}






